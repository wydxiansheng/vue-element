<template>
<div class="total">
<div class="total-header">
    <span></span>
    <router-link class="zong" to="/consolePage">总览</router-link>
    ><p class="comback">创建云分析</p>
</div>
<div class="outbox" style="background:#fff;">
    <child index="1" start="1" id="0" :type="$route.query.type"></child>
    <div class="CreateAnalysis_from_box">
        <div class="new-built">创建云分析</div>
        <div class="row createAnalysis-box">
            <div class="col-md-6">
                <div class="createAnalysis-list">
                    <div class="createAnalysis-list-title">
                        <span class="createAnalysis-fang">1</span>
                        请输入上云分析名称：
                    </div>                
                    <div class="create-yun">
                        <span class="create-radio-span">
                            <input type="radio" name="aaa" checked class="create-radio-input" v-on:click="clickI(1)">创建云分析
                        </span>
                        <span class="create-radio-span" v-if="existing.length>0">
                            <input type="radio"  name="aaa" class="create-radio-input" v-on:click="clickI(2)">选用现有云分析
                        </span>
                    </div>
                    <div class="clear"></div>
                    <div style="margin-top:20px;" >
                        <select v-if="radio2==true" id="select" class="create-select" v-model="changeyun" :class="ischangeyun==false?'error':''">
                            <option :value="item" v-for="item in existing">{{item.proname}}</option>
                        </select>
                        <input v-if="radio1==true" type="text" id="input" class="create-input" :class="isproName==false?'error':''"  v-model="proName" placeholder="请输入上云分析名称" v-on:blur="checkproname()">
                    </div>
                    <div class="clear"></div>
                    <div class="create-errornotice" v-if="isproName==false">{{Proerrornptice}}</div>
                    <div class="create-errornotice" v-if="ischangeyun==false">请选择现有云分析</div>
                </div>
                <div class="clear"></div>
                <div class="createAnalysis-list">
                    <div class="createAnalysis-list-title">
                        <span class="createAnalysis-fang">2</span>
                        请输入工作负载名称：
                    </div>
                    <input type="text" class="create-input" :class="isappName==false?'error':''"  v-model="appName" placeholder="请输入工作负载名称" v-on:blur="checkappname()">
                    <div class="clear"></div>
                    <div class="create-errornotice" v-if="isappName==false">{{appnameNotice}}</div>
                </div>
                <div class="createAnalysis-list">
                    <div class="createAnalysis-list-title">
                        <span class="createAnalysis-fang">3</span>
                        请选择工作负载类型：
                    </div>
                    <select class="create-select" v-model="type" :class="istype==false?'error':''" v-on:change="changeType()" >
                        <option :value="item.id" v-for="item in typeList">{{item.gname}}</option>
                    </select>
                    <div class="clear"></div>
                    <div class="create-errornotice" v-if="istype==false">请选择工作负载类型</div>
                </div>
                
                <div class="createAnalysis-list">
                    <div class="createAnalysis-list-title">
                        <span class="createAnalysis-fang">4</span>
                        请选择工作负载架构：
                    </div>
                    <select class="create-select" v-model="frame" :class="isframe==false?'error':''" v-on:change="changeFrame()" >
                        <option :value="item.id" v-for="item in frameList">{{item.gname}}</option>
                    </select>
                    <div class="clear"></div>
                    <div class="create-errornotice" v-if="isframe==false">请选择工作负载架构</div>
                </div>
                
                <div class="createAnalysis-list">
                    <div class="createAnalysis-list-title">
                        <span class="createAnalysis-fang">5</span>
                        请选择所属行业：
                    </div>
                    <select class="create-select" v-model="industry">
                        <option v-for="item in industryList" :value="item.id">{{item.name}}</option>
                    </select>
                </div>
                <div class="clear"></div>
                <div class="createAnalysis-list">
                    <div class="createAnalysis-list-title">
                        <span class="createAnalysis-fang">6</span>
                        请选择区域：
                    </div>
                    <div class="row" style="padding-left:30px;">
                        <div class="col-md-4" style="padding:0 !important;">
                            <select class="city-select" v-model="province" v-on:change="changeProvince(province)">
                                <option v-for="item in provinceList" :value="item">{{item.province}}</option>
                            </select>
                        </div>
                        <div class="col-md-4" style="padding:0 !important;">
                            <select class="city-select" v-model="city" v-on:change="changeCity(city)">
                                <option v-for="item in cityList" :value="item">{{item.city}}</option>
                            </select>
                        </div>
                        <div class="col-md-4" style="padding:0 !important;">   
                            <select class="city-select" v-model="area">
                                <option v-for="item in areaList" :value="item">{{item.area}}</option>
                            </select>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-6"></div>
            <!--<div class="col-md-4"></div>-->
        </div>
        <button class="nextbtn" v-on:click="submit()"><span style="margin-left:5px;">下一步</span><i class="iconfont icon-xiayibu" style="margin-left:5px;"></i></button>
        <div class="clear"></div>
    </div>
        
</div>
</div>
</template>
<script>
import child from '../../../../components/steps/steps.vue'
import '../createAnalysis/createAnalysis.css'
export default{
    name:'createAnalysis',
    data(){
        return {
            typeList:[],
            frameList:[],
            type:'',
            frame:'',
            analysisName:'',
            appName:'',
            existing:'',
            analysis_list:false,
            isanalysis:true,
            istype:true,
            isframe:true,
            isappName:true,
            proId:'',
            queryType:'',
            changeyun:'',
            isproName:true,
            proName:'',
            ischangeyun:true,
            radio1:true,
            radio2:false,
            industryList:[],
            industry:'',
            information:'',
            provinceList:[],
            cityList:[],
            areaList:[],
            province:'',
            city:'',
            area:'',
            Proerrornptice:'请输入上云分析名称',
            appnameNotice:'请输入工作负载名称'
        }
    },
    mounted:function(){
        this.information = JSON.parse(sessionStorage.getItem("account"));
        this.industry = this.information.industry;
        this.queryType = this.$route.query.type;
        this.province = JSON.parse(sessionStorage.getItem("account")).province;
        this.city = JSON.parse(sessionStorage.getItem("account")).city;
        this.area = JSON.parse(sessionStorage.getItem("account")).area;
        this.getProvince();
        //console.log('type',this.queryType);
        this.$this.get('/broker/app/types').then((response)=>{
            this.typeList = response.data.data;
        }).catch((error)=>{
            console.log(error);
        })
        this.$this.get('/broker/app/frames').then((response)=>{
            this.frameList = response.data.data;
        }).catch((error)=>{
            console.log(error);
        })
        //获取所有云分析名称
        this.$this.get('/broker/app/analysis').then((response)=>{
            this.existing = response.data.data;
            if(this.existing.length>0){
                this.changeyun = this.existing[0];
            }
            
            //console.log('aaa',response.data.data);
        }).catch((error)=>{
            console.log(error);
        })
        this.getIndustry();//行业
        $(document).keyup(function (evnet) {
            if (evnet.keyCode == '13') {
                return false;
            }
        });
    },
    methods:{
        changeFrame:function(){
            if(this.frame==''){
                this.isframe = false;
            }else{
                this.isframe = true;
            }
        },
        changeType:function(){
            if(this.type==''){
                this.istype = false;
            }else{
                this.istype = true;
            }
        },
        checkproname:function(){
            // console.log('----',this.proName);
            if(this.proName==''){
                this.isproName = false;
                this.Proerrornptice = '请输入上云分析名称';
            }else{
                this.$this.get('/broker/app/analysisname/judgment/'+this.proName).then((response)=>{
                    if(response.data.data>0){
                        this.isproName = false;
                        this.Proerrornptice = '当前上云分析名称已存在，请您重新命名。';
                    }else{
                        this.isproName = true;
                    }
                }).catch((error)=>{})
            }
            
        },
        checkappname:function(){
            if(this.radio2==true){
                if(this.appName==''){
                    this.isappName = false;
                    this.appnameNotice = '请输入工作负载名称';
                }else{
                    this.$this.get('/broker/app/appname/judgment/'+this.appName+'/'+this.changeyun.id).then((response)=>{
                        if(response.data.data>0){
                            this.isappName = false;
                            this.appnameNotice = '当前工作负载名称已存在，请您重新命名。';
                        }else{
                            this.isappName = true;
                        }
                    }).catch((error)=>{})
                } 

            }else{
                if(this.appName==''){
                    this.isappName = false;
                    this.appnameNotice = '请输入工作负载名称';
                }else{
                    this.isappName = true;
                }
            }
              
            
        },
        getIndustry:function(){
            this.$this.get('/broker/prop/industry/').then((response)=>{
                this.industryList = response.data.data;
                //console.log('province',response);
            }).catch((error)=>{
            })
        },
        getProvince:function(){
            this.$this.get('/broker/prop/provinces/').then((response)=>{
                this.provinceList = response.data.data;
                this.getCity(this.province.provinceid);
                //console.log('province',response);
            }).catch((error)=>{
            })
        },
        getCity:function(provinceid){
            this.$this.get('/broker/prop/citys/'+provinceid).then((response)=>{
                this.cityList = response.data.data;
                this.getArea(this.city.cityid);
                //console.log('city',response);
            }).catch((error)=>{
            })
        },
        getArea:function(cityid){
            this.$this.get('/broker/prop/areas/'+cityid).then((response)=>{
                this.areaList = response.data.data;
                //console.log('city',response);
            }).catch((error)=>{
            })
        },
        changeProvince:function(provinceid){
            this.city = '';
            this.area = '';
            this.getCity(provinceid.provinceid);
        },
        changeCity:function(city){
            this.area = '';
            this.getArea(city.cityid);
        },
        submit:function(){
            let proid,analysisName;
            if(this.radio1==true){
                //this.proId = 0;
                proid = 0;
                analysisName = this.proName;
            }else{
                proid = this.changeyun.id;
                analysisName = this.changeyun.proname; 
            }
            //console.log(this.changeyun);
            let obj = {
                "analysisName": analysisName,
                "appFrame": this.frame,
                "appName": this.appName,
                "appType": this.type,
                "proId":proid,
                "industry":this.industry,
                "provinceid":this.province.provinceid,
                "cityid":this.city.cityid,
                "areaid":this.area.areaid
            };
            let that = this;
            let str = JSON.stringify(obj);
            //console.log(this.radio1,'----',this.radio2);
            if(this.radio2==true){
                //console.log(this.changeyun.proname);
                this.reg2(str);
            }else if(this.radio1==true){//输入
                this.reg1(str);
            }else{
                this.regall();
            }
            //this.$router.push({path:'/resourceGroup'});
        },
        reg1:function(str){
            if(this.proName!=''&&this.type!=''&&this.frame!=''&&this.appName!=''){
                if(this.isproName==true){
                    this.isproName = true;
                    this.push(str);
                }
                this.istype = true;
                this.isframe = true;
                this.isappName = true;
            }else{
                this.checkproname();
                this.type == ''?this.istype = false:this.istype = true;
                this.frame == ''?this.isframe = false:this.isframe = true;
                if(this.appName==''){
                    this.isappName = false;
                    this.appnameNotice = '请输入工作负载名称';
                }else{
                    this.isappName = true;  
                }
                //this.appName ==''?this.isappName = false:this.isappName = true;  
            }
        },
        reg2:function(str){
            if(this.changeyun!=''&&this.type!=''&&this.frame!=''&&this.appName!=''){
                this.ischangeyun = true;
                this.istype = true;
                this.isframe = true;
                if(this.isappName==true){
                    this.isappName = true;
                    this.push(str);
                }
                
            }else{
                this.changeyun == ''?this.ischangeyun = false:this.ischangeyun = true;
                this.type == ''?this.istype = false:this.istype = true;
                this.frame == ''?this.isframe = false:this.isframe = true;
                //this.appName ==''?this.isappName = false:this.isappName = true; 
                this.checkappname(); 
            }
        },
        regall:function(){
            if(this.proName!=''&&this.ischangeyun!=''&&this.type!=''&&this.frame!=''&&this.appName!=''){
                this.ischangeyun = true;
                //this.isproName = true;
                this.istype = true;
                this.isframe = true;
                if(this.isappName==true){
                    this.isappName = true;
                }else if(this.isproName==true){
                    this.isproName = true;
                }
                //this.isappName = true;
            }else{
                this.changeyun == ''?this.ischangeyun = false:this.ischangeyun = true;
                //this.proName == ''?this.isproName = false:this.isproName = true;
                this.type == ''?this.istype = false:this.istype = true;
                this.frame == ''?this.isframe = false:this.isframe = true;
                //this.appName ==''?this.isappName = false:this.isappName = true; 
                this.checkproname(); 
                this.checkappname();
            }
        },
        clickI:function(ind){
            if(ind==1){
                if(this.radio1==false){
                    this.radio1=true;
                    this.radio2=false;
                    this.ischangeyun = true;
                    $("#select").attr("disabled",true);
                     $("#input").attr("disabled",false);
                }else{
                    this.radio1=false;
                    this.radio2=true;
                    this.isproName = true;
                    $("#input").attr("disabled",true);
                    $("#select").attr("disabled",false);
                }
            }else{
                if(this.radio2==false){
                    this.radio2=true;
                    this.radio1=false;
                    this.isproName = true;
                    $("#select").attr("disabled",false);
                    $("#input").attr("disabled",true);
                }else{
                    this.radio2=false;
                    this.radio1=true;
                    this.ischangeyun = true;
                    $("#input").attr("disabled",false);
                    $("#select").attr("disabled",true);
                }
            }
        },
        push:function(str){
            this.$this.post('/broker/app/analysis',str).then((response)=>{
                sessionStorage.setItem('appId',response.data.data);
                this.$router.push({path:'/resourceGroup',query:{type:this.queryType,id:response.data.data}});
            }).catch((error)=>{
                console.log(error);
            })
        },
        changeExist:function(name,id){//选择已有的云分析
            this.analysis_list = false;
            this.analysisName = name;
            this.proId = id;
        },
        changeclould:function(item){
            this.proId = item.id;
            this.analysisName = item.proname;
        }
    },
    components:{
        child
    }
}
</script>