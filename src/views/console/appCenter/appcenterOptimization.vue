<template>
<div class="total">
    <div class="total-header">
        <span></span>
        <router-link class="zong" to="/appcenterList">应用市场</router-link>
        ><p class="comback">多云价格优选分析助手</p>
    </div>
    <div class="appcenterPrice">
        <div class="appcplan-list"> 
            <el-form :model="matchBo" :rules="rules" ref="matchBo" label-width="80px">
                <el-form-item label="CPU" prop="cores" class="appcplan-from-item">
                    <el-input class="appcplan-input" type="number" min="1" placeholder="请输入CPU" v-model="matchBo.cores" v-on:blur="onblur('cores')"></el-input>
                </el-form-item>
                <el-form-item label="内存" prop="ram" class="appcplan-from-item">
                    <el-input class="appcplan-input" type="number" min="1" placeholder="请输入内存" v-model="matchBo.ram" v-on:blur="onblur('ram')"></el-input>
                </el-form-item>
               
                <el-form-item label="购买周期" prop="months" class="appcenter-from-select">
                    <el-select v-model="matchBo.months" placeholder="请选择购买周期">
                        <el-option v-for="item in month" :label="item.name" :value="item.months" :key="JSON.stringify(item.months)"></el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="区域" prop="region" class="appcenter-from-select">
                    <el-select v-model="matchBo.region" placeholder="请选择区域">
                        <el-option v-for="item in region" :label="item.region" :value="item.code" :key="JSON.stringify(item.code)"></el-option>
                    </el-select>
                </el-form-item>                                               
                <el-form-item class="appcplan-btn">
                    <el-button type="button" class="appcplan-button" v-on:click="submit('matchBo')">查询</el-button>
                </el-form-item>
            </el-form>
        </div>
        <div class="riu">
            <div class="appcheck-canvastitle" v-if="this.pricelist.length>0"><span></span>云实例匹配结果列表</div>
            <div id="designHalf-app" style="width:100%;height:300px;"></div>
            <div class="appcenterPrice-table" v-if="this.pricelist.length>0">
                <table>
                    <thead>
                        <tr>
                            <th>云厂商</th>
                            <th>产品名称</th>
                            <th>CPU</th>
                            <th>内存</th>
                            <th>选型评星</th>
                            <th>价格评星</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="it in pricelist">
                            <td>{{it.sname}}</td>
                            <td>{{it.pname}}</td>
                            <td>{{it.cores}}</td>
                            <td>{{it.ram}}</td>
                            <td><i v-for="(i,index) in 5" class="iconfont icon-xingxing" :class="it.serverStar>index?'startd-huang':'startd-ccc'"></i></td>
                            <td><i v-for="(i,index) in 5" class="iconfont icon-xingxing" :class="it.priceStar>index?'startd-huang':'startd-ccc'"></i></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
        <div class="nodata" v-show="proxyshow">
            <img src="../../../assets/compare-nodata.png" alt="">
            <br>
            暂无此信息，具体请联系Prof. 吴。
        </div>
    </div>
</div>
</template>
<style>
    .startd-huang{
         color:rgb(247, 167, 44);
    }
    .startd-ccc{
        color:#dfdfdf;
    }
</style>
<script>
import '../appCenter/appcenterPrice/appcenterPrice.css'
import echarts from 'echarts'
export default {
    name:'appcenterOptimization',
    data(){
        return {
            matchBo:{
                cores:'',
                ram:'',
                firm:'',
                region:'',
                months:''
            },
            gth:false,
            proxyshow:false,
            ist:false,
            appX:[],
            appXs:[],
            appEcharts:[],
            match:{
                "appMatchBo": {
                    "cores": '',
                    "ram": ''
                },
                "priceParamBo": {
                    "buyType": 1,//包年包月
                    "month": '',//购买周期
                    "paymentType": 1,//预付费
                    "regions": [],//区域
                    "serverId": -1//云厂商
                }
            },
            month:[
                {name:'1年',months:'12'},
                {name:'2年',months:'24'},
                {name:'3年',months:'36'},
                {name:'4年',months:'48'},
                {name:'5年',months:'60'},
            ],
            rules:{
                ram: [
                    { required: true, message: '请输入内存容量', trigger: 'blur,change' },
                ],
                cores: [
                    { required: true, message: '请输入CPU核数', trigger: 'blur,change' },
                ],
                firm:[
                    { required: true, message: '请选择云厂商', trigger: 'blur,change' },
                ],
                region:[
                    { required: true, message: '请选择区域', trigger: 'blur,change' },
                ],
                months:[
                    { required: true, message: '请选择购买周期', trigger: 'blur,change' },
                ]
            },
            clouldcompany:[],
            region:[],
            pricelist:[]
        }
    },
    mounted:function(){
        this.getCloudlist();
        this.getRegion(-1);
    },
    methods:{
        onblur:function(dom){
            if(dom=='cores'){
                this.matchBo.cores<0?this.matchBo.cores=1:this.matchBo.cores=this.matchBo.cores;
            }else if(dom=='ram'){
                this.matchBo.ram<0?this.matchBo.ram=1:this.matchBo.ram=this.matchBo.ram;
            }
        },
        getCloudlist:function(){
            this.$this.get('/broker/price/suppliers/list').then((res)=>{
               // console.log(res.data.data);
                for(let i=0;i<res.data.data.length;i++){                    
                    for(let n in res.data.data[i]){
                        this.clouldcompany.push({id:n,name:res.data.data[i][n]})
                    }
                }
            }).catch((error)=>{})
        },
        getRegion:function(id){
            this.$http.get('/broker/price/region/'+id).then((response)=>{
                //console.log('----',response.data.data);
                if(id==-1){
                    this.getRegion(response.data.data[0].id);
                }else{
                    this.region = response.data.data;
                }                
            }).catch((error)=>{
            })
        },
        hui:function(){
            
        },
        canversBar:function(dom,xdata,datalist,text){
            let that = this;
            this.charts = echarts.init(document.getElementById(dom));
           
            this.charts.setOption({              
                tooltip:{
                    trigger: 'axis',
                    axisPointer: {
                        type: 'cross',
                        crossStyle: {
                            color: '#999'
                        }
                    },
                },
                legend: {
                    data: [text],
                    x:'77%',
                    //right:'10px',
                    y:'10px'
                },
                xAxis: [{
                    name:'云厂商',
                    type:'category',
                    data: xdata,
                    axisPointer:{
                        type:'shadow'
                    },
                    axisLine: {
                        lineStyle: {
                            color: '#c2c2c2'
                        }
                    },
                    nameTextStyle:{
                        color:'#333'
                    },
                    nameLocation:'end',
                    axisLabel: {  
                        interval:0,  
                        rotate:30  
                    } 
                }],
                yAxis: [{
                    type:'value',
                    name:'价格',
                    axisLabel: {
                        formatter: '{value}'
                    },
                    axisLine: {
                        lineStyle: {
                            color: '#c2c2c2'
                        }
                    },
                    nameTextStyle:{
                        color:'#333'
                    },
                }],
                series: [
                    {
                        name:text,
                        type:'bar',
                        data:datalist,
                        itemStyle:{
                            normal:{
                                color:'#f7a72c'
                            }
                        },
                        barWidth : 25,//柱图宽度
                    }
                ]
            })
        },
        submit:function(value){
            this.$refs[value].validate((valid) => {
                if (valid) {
                  
                     this.pricelist = [];
                     this.appX = [];
                     this.appEcharts  = [] ;
                     this.appXs = []; 
                    this.match.appMatchBo.cores = this.matchBo.cores;
                    this.match.appMatchBo.ram = this.matchBo.ram;
                    this.match.priceParamBo.month = this.matchBo.months;
                    this.match.priceParamBo.regions.push(this.matchBo.region);
                   
                    this.$this.post('/broker/app/math/calc/price',JSON.stringify(this.match)).then((response)=>{
                    this.pricelist = response.data.data;
                    if(this.pricelist.length==0){
                           $(".riu").hide();
                            this.proxyshow = true;
                    }else if(this.pricelist.length>0){
                        $(".riu").show();
                        this.proxyshow = false;
                        this.appX = this.pricelist.slice(0,5);
                        for(var a = 0 ;a<this.appX.length;a++){
                        
                            this.appXs.push(this.appX[a].cloudPrice)
                            this.appEcharts.push(this.appX[a].sname+'/'+this.appX[a].pname);
                        }
                            console.log(this.appEcharts)
                        this.canversBar('designHalf-app',this.appEcharts,this.appXs,'云厂商应用规格');
                     }       
                       
                    }).catch((error)=>{})
                } else {
                    return false;
                }
            });
        },
    }
}
</script>

