<template>
<div class="total">
<div class="total-header">
    <span></span>
    <router-link class="zong" to="/consolePage">总览</router-link>
    ><p class="comback" v-on:click="goBack()">云选型</p>
    ><p class="comback">选择标准</p>
</div>
<child index="4" start="3" :type="$route.query.type" :id="$route.query.id"></child>
<div class="compare-line"></div>
<div class="compare-container">
    <div class="compare-title">选型标准</div>
    <!-- 云厂商选择 -->
    <div class="compare-change">
        <div class="change-select">云厂商选择</div>
        <div class="row">
            <div class="change-name col-md-1"></div>
            <div class="change-list col-md-11 row">
                <div class="all-list col-md-11 ulas row">
                    <div class="col-md-1 compare-change-key">云厂商：</div>
                    <div class="change-all col-md-1" v-on:click="allprovider()">全选</div>
                    <ul class="col-md-10">
                        <li id="lis" v-for="(item,index) in providerList" :class="item.boolean==true?'active-change':'default'" v-on:click="providerChange(index)">{{item.data.sname}}</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    <!-- 场景选择 -->
    <div class="compare-change">
        <div class="change-select">场景选择</div>
        <div class="row">
            <div class="change-name col-md-1"></div>
            <div class="change-list col-md-11 row">
                <div class="all-list col-md-11 ulas row" v-for="(types,index) in typelist">
                    <div class="col-md-1 compare-change-key">{{types.gname}}：</div>
                    <div class="change-all col-md-1" v-on:click="allSelect(index)">全选</div>
                    <ul class="col-md-10">
                        <li id="lis" v-for="(typeChild,indexes) in types.childGroups" :class="typeChild.selected==true?'active-change':'default'" v-on:click="changeType(index,indexes)">{{typeChild.gname}}</li>
                    </ul>
                </div>
            <!--<ul class="all-list col-md-11 ulas"  v-for="(types,index) in typelist">
                    <li class="default">
                        {{types.gname}}：
                </li>
                    <li class="change-all col-md-1" v-on:click="allSelect(index)">全选</li>
                <li id="lis" v-for="(typeChild,indexes) in types.childGroups" :class="typeChild.selected==true?'active-change':''" v-on:click="changeType(index,indexes)">{{typeChild.gname}}</li>
                </ul>-->
            </div>
        </div>
    </div>
    <!-- 空白 -->
    <div class="nodata" v-if="typeCheck.length<1">
        <img src="../../../../assets/compare-nodata.png" alt="">
        <br>
        
        暂无数据

    </div>
    <!-- 做题 -->
    <div v-for="(out,i) in firsttitle" v-else style="margin-top:20px;">
        <div class="compare-question-title" v-if="out.selected==true" style="background:#dedede;">
            <span>{{out.gname}}</span>
            <span class="add-toggle" v-on:click="zong(i)">+</span>
        </div>
        <div><!-- v-if="numlist[i].boolean==true"-->
            <div class="compare-box" v-for="(item,index) in typeCheck" v-if="item.type.gname==out.gname">
                <div class="compare-question-title">
                    <span>{{item.name}}</span>
                    <span class="add-toggle" v-on:click="toggle(item,index)">+</span>
                </div>
                <ul class="compare-question-list" v-if="item.boolean==true">
                    <li class="row" v-for="(list,i) in item.data">
                        <p class="col-md-6">
                            <span class="compare-num">Q</span><!-- Q{{i+1}}. -->
                            {{list.content}}
                        </p>
                        <p class="col-md-6">
                            <select class="compare-select" v-model="valuelist[list.id]" v-on:change="changeSelect(list)">
                                <option :value="option" v-for="option in optionlist">{{option.name}}</option>
                            </select>
                        </p>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="comparebnt-box">
        <button class="comparebtn" v-on:click="result()">
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
import '../compareQuestion/compareQuestion.css'
export default{
    name:'compareQuestion',
    data(){
        return {
            queryType:'',
            typelist:[],
            groups:[],
            typeCheck:[],
            optionlist:[],
            valuelist:{},
            togglelist:[],
            havelist:[],
            numlist:[],
            allLsit:[],
            Ind:0,
            allindex:0,
            providerList:[],
            providerId:[],
            firsttitle:[]
        }
    },
    mounted:function(){
        this.queryType = this.$route.query.type;
        this.appId = this.$route.query.id; 
        this.getTypes();
        this.getOptions();
        this.getprovider();//云厂商列表
    },
    methods:{
        allprovider:function(){
            let index=0;
            for(let j=0;j<this.providerList.length;j++){
                if(this.providerList[j].boolean==false){
                    index++;
                }
            }
            if(index>0){
                for(let j=0;j<this.providerList.length;j++){
                    this.providerList[j].boolean = true;
                }
            }else{
               for(let j=0;j<this.providerList.length;j++){
                    this.providerList[j].boolean = false;
                } 
            }
        },
        providerChange:function(index){
            this.providerList[index].boolean==false?this.providerList[index].boolean=true:this.providerList[index].boolean=false;
        },
        getprovider:function(){//云厂商列表
           this.$this.get('/broker/compare/cloud/provider/'+this.appId).then((response)=>{
                for(let i=0;i<response.data.data.all.length;i++){
                    this.providerList.push({boolean:false,data:response.data.data.all[i]});
                }
                if(response.data.data.active.length>0){
                    for(let n=0;n<response.data.data.active.length;n++){
                        for(let j=0;j<this.providerList.length;j++){
                            if(response.data.data.active[n]==this.providerList[j].data.id){
                                this.providerList[j].boolean = true;
                            }
                        }
                    }
                }else{
                    for(let k=0;k<this.providerList.length;k++){
                        this.providerList[k].boolean = true;
                    }
                }
                
           }).catch((error)=>{})
        },
        getTypes:function(){
            this.$this.get('/broker/compare/types/'+this.appId).then((response)=>{
                //console.log('----',response.data.data);
                this.typelist = response.data.data;
                this.havelist = response.data.data;
                let arr =[];
                let arry = [];
                this.firsttitle = [];//选中的最大标题
                for(let n=0;n<response.data.data.length;n++){
                    this.allLsit.push({boolean:false});
                    if(response.data.data[n].selected==true){
                        this.firsttitle.push(response.data.data[n]);
                    }
                    for(let i=0;i<response.data.data[n].childGroups.length;i++){
                        this.numlist.push({boolean:true});
                        if(response.data.data[n].childGroups[i].selected==true){
                            arr.push(response.data.data[n].childGroups[i].selected);
                            this.questionList(response.data.data[n].childGroups[i].id,true,n);
                            this.numlist[i].boolean = true;
                        }
                    }
                }  
                if(arr.length<1){
                    this.$alert('请首先选择场景进行答题。', '温馨提示', {
                        confirmButtonText: '我知道了',
                        showClose:false,
                        type: 'warning',
                        confirmButtonClass:'lay-btn-red'
                    });
                }          
            }).catch((error)=>{
                
            })
        },
        getOptions:function(){
            this.$this.get('/broker/compare/feature/option').then((response)=>{
                //console.log('ccc',response);
                this.optionlist =  response.data.data;                
            }).catch((error)=>{
                
            })
        },
        zong:function(ind){
            if(this.numlist[ind].boolean == false){
                this.numlist[ind].boolean=true;
            }else{
                this.numlist[ind].boolean=false;
            }
        },
        changeType:function(Ind,index){
            if(this.typelist[Ind].childGroups[index].selected==false){
                this.typelist[Ind].childGroups[index].selected=true;
                this.questionList(this.typelist[Ind].childGroups[index].id,true,Ind,this.typelist[Ind].childGroups[index].gname);
            }else{
                this.typelist[Ind].childGroups[index].selected=false;
                let aindex = 0;
                for(let i=0;i<this.typelist[Ind].childGroups.length;i++){
                    if(this.typelist[Ind].childGroups[i].selected==true){
                        aindex++;
                    }
                }
                if(aindex>0){
                    this.typelist[Ind].selected = true;
                }else{
                    this.typelist[Ind].selected = false;
                }
                this.questionList(this.typelist[Ind].childGroups[index].id,false,Ind,this.typelist[Ind].childGroups[index].gname);
            }
            // for(let i=0;i<this.havelist.length;i++){
            //     this.typelist[i].selected = this.havelist[i].selected;
            // }
            for(let i=0;i<this.typelist.length;i++){
                for(let n=0;n<this.typelist[i].childGroups.length;n++){
                    if(this.typelist[i].childGroups[n].selected==true){
                        this.typelist[i].selected = true;
                    }
                }
            }
            this.firsttitle = [];//选中的最大标题
            //let aa = [];
            for(let i=0;i<this.typelist.length;i++){
                if(this.typelist[i].selected==true){
                    if(this.typelist[i].gname!=this.typelist[Ind].gname){
                        this.firsttitle.push(this.typelist[i]);
                        //aa.push(this.typelist[i].gname);
                    }
                }
            }
            //console.log(aa);
            if(this.typelist[Ind].selected==true){
                this.firsttitle.push(this.typelist[Ind]);
            }
        },
        questionList:function(Id,boolean,Index,listname){
            let ax;
            for(let j=0;j<this.typelist.length;j++){
                for(let a=0;a<this.typelist[j].childGroups.length;a++){
                    if(this.typelist[j].childGroups[a].id==Id){
                        ax = a;
                    }                    
                }
            }
            if(boolean==true){
                this.$this.get('/broker/compare/feature/'+this.appId+'/'+Id+'').then((response)=>{
                        this.typeCheck.push({boolean:true,type:this.typelist[Index],data:response.data.data,name:this.typelist[Index].childGroups[ax].gname});                   
                        for(let n=0;n<this.typeCheck.length;n++){
                            for(let v=0;v<this.typeCheck[n].data.length;v++){
                                //this.valuelist.push(this.typeCheck[n].data[v].id);
                                //this.valuelist[this.typeCheck[n].data[v].id] = '';
                                // 默认选中
                                if(this.typeCheck[n].data[v].selectOptId!=null){
                                    //this.valuelist[this.typeCheck[n].data[v].id] = this.optionlist[this.typeCheck[n].data[v].selectOptId];
                                    this.valuelist[this.typeCheck[n].data[v].id] = this.optionlist[this.typeCheck[n].data[v].selectOptId-1];
                                }
                            }
                        }
                }).catch((error)=>{ 
                }) 
            }else{
                let that = this;
                this.typeCheck.forEach(function(value,index){
                    if(value.name==listname){
                        that.typeCheck.splice(index,1);
                    }
                })
            } 
        },
        changeSelect:function(item){
            let obj = {
                "appid": this.appId,
                "featureCode":item.code,//问题的code
                //"groupId": item.groupId,
                "optionId": this.valuelist[item.id].id//选项的id
            };
            let strObj = JSON.stringify(obj);
            this.$this.post('/broker/compare/saveUser',strObj).then((response)=>{            
            }).catch((error)=>{
            })
        },
        toggle:function(item,Index){
            if(this.typeCheck[Index].boolean==true){
                this.typeCheck[Index].boolean=false;
            }else{
                this.typeCheck[Index].boolean=true;
            }
        },
        result:function(){
            // this.$router.push({path:'/design',query:{id:this.appId,type:this.queryType}});
            let index = 0;
            for(let i=0;i<this.providerList.length;i++){
                if(this.providerList[i].boolean==true){
                    this.providerId.push(this.providerList[i].data.id);
                    index++;
                }
            }
            if(index>0){
                this.$router.push({path:'/compareResult',query:{id:this.appId,type:this.queryType,cloudId:this.providerId}});
            }else{
                this.$alert('请您至少选择一个云厂商进行云优选。', '温馨提示', {
                    confirmButtonText: '我知道了',
                    showClose:false,
                    type: 'warning',
                    confirmButtonClass:'lay-btn-red'
                });
            }
            
        },
        allSelect:function(e){
            //console.log(this.typelist);
            if(this.allLsit[e].boolean==false){
                this.allLsit[e].boolean=true;
                this.typelist[e].selected = true;
                for(let i=0;i<this.typelist[e].childGroups.length;i++){
                    if(this.typelist[e].childGroups[i].selected==false){
                        this.questionList(this.typelist[e].childGroups[i].id,true,e);
                        this.typelist[e].childGroups[i].selected=true;
                    }
                }
            }else{
                this.allLsit[e].boolean=false;
                this.typelist[e].selected = false;
                for(let i=0;i<this.typelist[e].childGroups.length;i++){
                    if(this.typelist[e].childGroups[i].selected==true){
                        this.questionList(this.typelist[e].childGroups[i].id,false,e,this.typelist[e].childGroups[i].gname);
                        this.typelist[e].childGroups[i].selected=false;
                    }
                }
            }
            this.firsttitle = [];//选中的最大标题
            for(let i=0;i<this.typelist.length;i++){
                if(this.typelist[i].selected==true){
                    if(this.typelist[i].gname!=this.typelist[e].gname){
                        this.firsttitle.push(this.typelist[i]);
                    }                    
                }
            }
            if(this.typelist[e].selected==true){
                this.firsttitle.push(this.typelist[e]);
            }
            
        },
        goBack:function(){
            this.$router.push({path:'/compareList'});
        },
        prev:function(){
            this.$router.push({path:'/planResult',query:{id:this.appId}});
        }
    },
    components:{
        child
    }
}
</script>