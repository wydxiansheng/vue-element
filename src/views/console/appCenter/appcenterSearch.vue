<template>
<div class="total">
    <div class="total-header">
        <span></span>
        <router-link class="zong" to="/appcenterList">应用市场</router-link>
        ><p class="comback">云实例快搜器</p>
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
                <el-form-item label="云厂商" prop="firm" class="appcenter-from-select">
                    <el-select v-model="matchBo.firm" placeholder="请选择云厂商">
                        <el-option v-for="item in clouldcompany" :label="item.name" :value="item.id" :key="JSON.stringify(item.id)"></el-option>
                    </el-select>
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
        <div v-if="pricelist.length>0" class="appcheck-canvastitle"><span></span>云实例匹配结果列表</div>
        <div class="appcenterPrice-table">
            <table>
                <thead>
                    <tr>
                        <th>云厂商</th>
                        <th>产品名称</th>
                        <th>CPU</th>
                        <th>内存</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="it in pricelist">
                        <td>{{it.sname}}</td>
                        <td>{{it.pname}}</td>
                        <td>{{it.cores}}</td>
                        <td>{{it.ram}}</td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="nodata" v-if="proxyshow==true">
            <img src="../../../assets/compare-nodata.png" alt="">
            <br>
            暂无此信息，具体请联系Prof. 吴。
        </div>
    </div>
</div>
</template>
<style>
     .notification-undata{
        /*background:#ffffff; width:100%; height:100%; font-size:14px; color:#555; margin:10px 0;line-height:30px; text-align:center; padding-bottom:16%;*/
        background:#ffffff;
        width:100%;
        height:300px;
        font-size:12px;
        color:#999;
        margin-bottom:20px;
        line-height:24px;
        text-align:center;
        border:1px solid #ebebeb;
   }
   .notification-undata img{
       /*margin-top:20%;*/
       margin-top:100px;
        margin-bottom:20px;
   }
</style>
<script>
import '../appCenter/appcenterPrice/appcenterPrice.css'
export default {
    name:'appcenterPrice',
    data(){
        return {
            matchBo:{
                cores:'',
                ram:'',
                firm:'',
                region:'',
                months:''
            },

            proxyshow:false,

            hello:false,
            world:false,

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
                    "serverId": ''//云厂商
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
        submit:function(value){
            this.$refs[value].validate((valid) => {
                if (valid) {
                    this.proxyshow = false;
                    this.match.appMatchBo.cores = this.matchBo.cores;
                    this.match.appMatchBo.ram = this.matchBo.ram;
                    this.match.priceParamBo.month = this.matchBo.months;
                    this.match.priceParamBo.regions.push(this.matchBo.region);
                    this.match.priceParamBo.serverId = this.matchBo.firm;
                    this.$this.post('/broker/app/math/calc/price',JSON.stringify(this.match)).then((response)=>{
                        //console.log('---',response.data);
                        this.pricelist = response.data.data;
                        if(this.pricelist.length==0){
                            this.proxyshow = true
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

