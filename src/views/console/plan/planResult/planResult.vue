<template>
<div class="total">
<div class="total-header">
    <span></span>
    <router-link class="zong" to="/consolePage">总览</router-link>
    ><p class="comback" v-on:click="goBack('planquestion')">云规划</p>
    <!--<p class="comback" v-on:click="goBack('planquestion')">选择标准</p>-->
    ><p class="comback">云规划报表</p>
</div>
<child index="3" start="3" :type="$route.query.type" :id="$route.query.id"></child>
<div class="plan-box">
    <div class="compare-start">
        <!--<button class="startbtn" v-on:click="compare()">开始云选型</button>-->
            <!--<button class="btn btn-default importbtn">导出</button>-->
        <div class="clear"></div>
    </div>
    <!--<div class="legend-box">
        <div class="legend">  
            <div class="legend-list">
                <span class="legend-block legend-high"></span>
                高
            </div>   
            <div class="legend-list">
                <span class="legend-block legend-heshi"></span>
                合适
            </div>
            <div class="legend-list">
                <span class="legend-block legend-yib"></span>
                一般
            </div>
            <div class="legend-list">
                <span class="legend-block legend-di"></span>
                低
            </div>
        </div>-->
        <div class="result-echarts" id="main"></div>
    </div>
    <div class="echarts-desc">工作负载分布图</div>
    <div class="row">
        <div class="col-md-3">
            <p class="appname">
                <span>{{result.proname}}</span>
                <span>{{result.appname}}</span>
            </p>
        </div>
        <div class="col-md-3 clould-result" v-for="item in resultlist">
            <p class="score" :class="item.moduleId==1?'score-qualitative':item.moduleId==2?'score-profit':'score-affinity'">
                <span class="score-name" v-if="item.moduleId!=1">{{item.moduleName}}</span>
                <span class="score-name" v-else>{{item.moduleName}}</span>
                <span class="score-val" v-if="item.moduleId!=1">{{item.result}}</span>
                <span class="score-val" v-else>{{JSON.parse(item.result).sname}}</span>
            </p>
        </div>
    </div>
    <div class="clould-desc" v-html="desc"></div>
    <div class="planResult-btn" style="margin-top:20px;">
        <button class="planbtn" v-on:click="compare()">
            <span class="pl-10">下一步</span><i class="iconfont icon-xiayibu" style="margin-left:5px;"></i>
        </button>
        <button class="planprev" v-on:click="prev()">
            <i class="iconfont icon-shangyibu1" style="margin-right:5px;"></i><span class="pr-5">上一步</span>
        </button>
    </div>
    <div class="clear"></div>
</div>
</div>
</template>
<script>
import child from '../../../../components/steps/steps.vue'
import '../planResult/planResult.css'
import echarts from 'echarts'
export default{
    name:'planResult',
    data(){
        return {
            charts:'',
            opiniondata:[],
            appId:'',
            result:{},
            queryType:'',
            resultlist:[],
            desc:'',
            isclick:'',
        }
    },
    mounted:function(){
        this.queryType = this.$route.query.type;
        //this.appId = sessionStorage.getItem('appId');
        this.appId = this.$route.query.id;
        //console.log(this.appId);
        //结果
        this.$this.get('/broker/result/plan/'+this.appId+'').then((response)=>{
            //console.log('结果',response);
            let qinhe,shouyi;   
            this.result =  response.data.data; 
            for(let i=0;i<response.data.data.appResults.length;i++){
                if(response.data.data.appResults[i].moduleId==1||response.data.data.appResults[i].moduleId==2||response.data.data.appResults[i].moduleId==3){
                    this.resultlist.push(response.data.data.appResults[i]);
                }
                if(response.data.data.appResults[i].moduleId==2){
                    shouyi = response.data.data.appResults[i].result;
                }
                if(response.data.data.appResults[i].moduleId==3){
                    qinhe = response.data.data.appResults[i].result;
                }
                if(response.data.data.appResults[i].moduleId==1){
                    this.desc = JSON.parse(response.data.data.appResults[i].result).description;
                    this.isclick = JSON.parse(response.data.data.appResults[i].result).id;
                }
            }
            this.opiniondata =  [{
                name:response.data.data.appname,
                value:[shouyi,qinhe]
            }] 
            this.$nextTick(function() {
                this.drawPie('main')
            })
            //console.log('----',this.opiniondata);         
        }).catch((error)=>{
        }) 
        
    },
    methods:{
        compare:function(){
            //alert(this.isclick);
            //this.$router.push({path:'/compareQuestion',query:{id:this.appId}});
            //if( this.isclick!=1 && this.isclick!=2 ){
            if( this.isclick!=1){//物理机
                this.$router.push({path:'/compareQuestion',query:{id:this.appId}});
            }else{
                let that = this;
                this.$alert('因在云规划后不属于公有云服务类型，所以后台将助您直接进入综合报告。', '温馨提示', {
                    confirmButtonText: '我知道了',
                    showClose:false,
                    confirmButtonClass:'lay-btn-red',
                    type: 'warning',
                    callback:function(action){
                        that.$router.push({path:'/colligateReport',query:{id:that.appId,type:that.queryType}});
                    }
                });
                
            }            
        },
        drawPie:function(id){
           // console.log(this.opiniondata);
            this.charts = echarts.init(document.getElementById(id));
            this.charts.setOption({
                //backgroundColor:'#ccc',
                title: {
                    text: this.result.proname+' '+this.result.appname +'云规划报告',
                    textStyle:{
                        color:'#333333',
                        fontWeight:'bold',
                        fontSize:'15'
                    },
                    left: 'center'
                },
                tooltip: {
                    trigger: 'item',
                    axisPointer: {
                        show: true,
                        type: 'cross',
                        lineStyle: {
                            type: 'dashed',
                            width: 1
                        }                        
                    },
                    formatter: function(obj) {
                        if (obj.componentType == "series") {
                            return '<div style="border-bottom: 1px solid rgba(255,255,255,.3); font-size: 18px;padding-bottom: 7px;margin-bottom: 7px">' +
                                obj.name +
                                '</div>' +
                                '<span>' +
                                '云亲和度' +
                                '</span>' +
                                ' : ' + obj.data.value[0]  +
                                '<br/>' +
                                '<span>' +
                                '云收益度' +
                                '</span>' +
                                ' : ' + obj.data.value[1] 
                        }
                    }
                },
                label: {
                    normal: {
                        show: true,
                        position: 'bottom',
                        formatter: function(params) {
                            return params.name
                        }
                    },
                    emphasis: {
                        show: true,
                        position: 'bottom',
                    }
                },
                xAxis: {
                    name: '云收益度',
                    type: 'value',
                    scale: true,
                    min:0,
                    max:100,
                    interval:10,
                    axisLabel: {
                        interval:0
                    },
                    splitLine: {
                        show: false
                    },
                    axisLine: {
                        lineStyle: {
                            color: '#c2c2c2'
                        }
                    },
                    nameTextStyle:{
                        color:'#333'
                    }
                },
                yAxis: {
                    name: '云亲和度',
                    type: 'value',
                    scale: true,
                    min:0,
                    max:100,
                    interval:10,
                    axisLabel: {
                        interval:20
                    },
                    splitLine: {
                        show: false
                    },
                    axisLine: {
                        lineStyle: {
                            color: '#c2c2c2',
                            width:'2'
                        }
                    },
                    nameTextStyle:{
                        color:'#333'
                    }
                },
                visualMap: {
                    min: 0,
                    max: 100,
                    dimension: 0,
                    right:'5%',
                    //left: '73%',
                    top: '10',
                    text: ['高', '低'], // 文本，默认为数值文本
                    calculable: false,
                    itemWidth: 10,
                    itemHeight: 90,
                    textStyle: {
                        color: '#666',
                        height: 56,
                        fontSize: 11,
                        lineHeight: 60,
                    },
                    inRange: {
                        color: ['yellow', '#da121a']
                    },
                    //padding: [50, 20],
                    orient: 'horizontal',
                },
                series: [{
                    type: 'scatter',
                    data: this.opiniondata,
                    symbolSize: 13,
                    markLine: {
                        lineStyle: {
                            normal: {
                                color: "#f7a72c",
                                type: 'solid',
                                width: 1,
                            },
                            emphasis: {
                                color: "#d9def7"
                            }
                        },
                        data: [{
                            xAxis: 50,
                            name: '平均线',
                            itemStyle: {
                                normal: {
                                    color: "#b84a58",
                                }
                            }
                        }, {
                            yAxis: 50,
                            name: '平均线',
                            itemStyle: {
                                normal: {
                                    color: "#b84a58",
                                }
                            }
                        }]
                    },
                    markArea: {
                        silent: true,
                        data: [
                            [{
                                name: '',//合适
                                itemStyle: {
                                    normal: {
                                        color: '#fff'
                                    },
                                },
                                label: {
                                    normal: {
                                        show: true,
                                        position: 'insideTopLeft',
                                        fontStyle: 'normal',
                                        color: "#fff",
                                        fontSize: 20,
                                    }
                                },
                                coord: [50, 50],
                            }, {
                                coord: [Number.MAX_VALUE, 0],
                            }],
                            [{
                                name: '',//低
                                itemStyle: {
                                    normal: {
                                        color: '#fff',
                                    },
                                },
                                label: {
                                    normal: {
                                        show: true,
                                        position: 'insideTopRight',
                                        fontStyle: 'normal',
                                        color: "#fff",
                                        fontSize: 20,
                                    }
                                },
                                coord: [0, 0],
                            }, {
                                coord: [50, 50],
                            }],
                            [{
                                name: '',//高
                                itemStyle: {
                                    normal: {
                                        color: '#fff',
                                    },
                                },
                                label: {
                                    normal: {
                                        show: true,
                                        position: 'insideBottomLeft',
                                        fontStyle: 'normal',
                                        color: "#fff",
                                        fontSize: 20,
                                    }
                                },
                                coord: [50, 50],
                            }, {
                                coord: [Number.MAX_VALUE, Number.MAX_VALUE],
                            }],
                            [{
                                name: '',//一般
                                itemStyle: {
                                    normal: {
                                        color: '#fff',
                                    },
                                },
                                label: {
                                    normal: {
                                        show: true,
                                        position: 'insideBottomRight',
                                        fontStyle: 'normal',
                                        color: "#fff",
                                        fontSize: 20,
                                    }
                                },
                                coord: [0, Number.MAX_VALUE],
                            }, {
                                coord: [50, 50],
                            }],
                        ]
                    }
                }]
                //
            })
        },
        goBack:function(link){
            if(link=='planlist'){
                this.$router.push({path:'/planList'});
            }else if(link=='planquestion'){
                this.$router.push({path:'/planQuestion',query:{id:this.appId,name:'1'}});
            }
        },
        prev:function(){
            this.$router.push({path:'/planQuestion',query:{id:this.appId,name:'1'}});
        }
    },
    components:{
        child
    }
}
</script>