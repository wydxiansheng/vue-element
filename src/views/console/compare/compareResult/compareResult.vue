<template>
<div class="total">
<div class="total-header">
    <span></span>
    <router-link class="zong" to="/consolePage">总览</router-link>
    ><p class="comback" v-on:click="goBack('comparelist')">云选型</p>
    ><p class="comback" v-on:click="goBack('comparequestion')">选择标准</p>
    ><p class="comback">选型报告</p>
</div>
<child index="4" start="3" :type="$route.query.type" :id="$route.query.id"></child>
<div class="compare-line"></div>
<div class="compareResult-box">
    <div class="compare-title">分析供应商</div>
    <div class="compare-cate">云供应商选型结果</div>
    <table class="table-score">
        <thead>
            <tr>
                <th v-if="planSid==2 || planSid==3">选择意向厂商</th>
                <th>云供应商</th>
                <th>分数</th>
                <th>官网地址</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="item in compareResultList">
                <td class="text-center col-md-2" v-if="planSid==2 || planSid==3">
                    <input type="checkbox" :value="item.sid" v-model="inserver" v-on:change="intentionServer(item.sid,$event)">
                </td>
                <td>{{item.serverName}}</td>
                <td>{{item.scope}}</td>
                <td>
                    <a target="_blank" style="color:rgb(51, 122, 183) !important;" :href="item.sid==7?'https://ecs-buy.aliyun.com/':item.sid==8?'https://aws.amazon.com/cn/pricing/?nc2=h_ql_pr&awsm=ql-3':item.sid==9?'https://www.azure.cn/pricing/overview/':item.sid==10?'https://buy.cloud.tencent.com/price/cvm/calculator':item.sid==11?'https://portal.huaweicloud.com/pricing#ecs':item.sid==12?'https://www.qingcloud.com/pricing#/InstancesKVM':item.sid==13?'https://www.vmware.com/cn.html':item.sid==14?'https://www.openstack.org/community':item.sid==15?'http://e.huawei.com/cn/solutions/technical/Cloud-Computing':item.sid==16?'https://www.aliyun.com/solution/dedicatedcloud':item.sid==17?'http://www.h3c.com/cn/Solution/TechnologySolution/CloudComputing/':item.sid==18?'http://www.china-entercom.com/cn/product-services/smartcloud-vone':''"><i class="iconfont icon-lianjie font12" style="margin-right:5px;"></i>参考链接</a>
                </td>
            </tr>
        </tbody>
    </table>
    <div class="compare-cate">云供应商标准选型差异</div>
    <div>
        <p class="explain">
            <span><i class="iconfont icon-yuan high-ratio" style="margin-right:3px;"></i>高匹配</span>
            <span><i class="iconfont icon-yuan low-ratio" style="margin-right:3px;"></i>低匹配</span>
        </p>
    </div>
    <div class="clear"></div>
    <div class="difference-box">
        <table class="comdetails-table">
            <thead>
                <tr>
                    <th class="obliqueline" colspan="3">
                        <span class="clould-profirm">云供应商</span>
                        <span class="clould-details">场景</span>
                    </th>
                    <th v-for="firm in confirm">{{firm.service}}</th>
                </tr>
            </thead>
            <tbody v-for="(item,index) in details">
                <tr class="comdetails-tab-title">
                    <td :colspan="length">{{index}}</td>
                </tr>
                <tr class="comdetails-tab-list" v-for="list in item">
                    <td style="width:10%;"></td>
                    <td class="textleft">{{list.feature}}</td>
                    <td>{{list.servers[0].compareopt}}</td>
                    <td v-for="aa in list.servers">
                        <i class="iconfont icon-yuan" :class="aa.type==1?'high-ratio':'low-ratio'"></i>
                        <!--<i class="iconfont icon-yuan" v-else :class="aa.type!=1?'orange':''"></i>-->
                        <!--<img v-if="aa.type==1" src="../../../../assets/compare/compare-right.png" alt="">
                        <img v-else src="../../../../assets/compare/compare-cha.png" alt="">-->
                    </td>
                    <!--aa.type=1是有 0 是没有 -->
                </tr>
            </tbody>
        </table>
    </div>
    <!-- <div class="compare-cate" v-if="res==true">上云工作负载配置信息详情</div>
    <table class="table-score resourGroup-table" v-if="res==true">
        <thead v-if="appServer.length>0||dbServer.length>0||network!=null||storage.length>0||cdns.length>0">
            <tr>
                <th>数量</th>
                <th>资源</th>
                <th>规格</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="item in appServer">
                <td>{{item.num}}</td>
                <td>应用服务</td>
                <td>
                    <p><span class="labelRed">{{item.cores}}</span>（v）CPU</p>
                    <p><span class="labelRed">{{item.ghz}}</span>处理器主频（GHZ）</p>
                    <p><span class="labelRed">{{item.ram}}</span>内存（GB）</p>
                    <p><span class="labelRed">{{item.localDisk}}</span>系统盘（GB）</p>
                    <p><span class="labelRed">{{item.os}}</span>操作系统</p>
                    <p><span class="labelRed">{{item.computeMappingFactor}}</span>资源平均利用率</p>
                </td>
            </tr>
            <tr v-for="db in dbServer">
                <td>{{db.num}}</td>
                <td>数据库服务</td>
                <td>
                    <p><span class="labelRed">{{db.cores}}</span>（v）CPU</p>
                    <p><span class="labelRed">{{db.ghz}}</span>处理器主频（GHZ）</p>
                    <p><span class="labelRed">{{db.ram}}</span>内存（GB）</p>
                    <p><span class="labelRed">{{db.localDisk}}</span>系统盘（GB）</p>
                    <p><span class="labelRed">{{db.os}}</span>操作系统</p>
                    <p><span class="labelRed">{{db.computeMappingFactor}}</span>资源平均利用率</p>
                </td>
            </tr>
            <tr v-if="network!=null">
                <td></td>
                <td>网络存储</td>
                <td>
                    <p><span class="labelRed">{{network.bandwidth}}</span>带宽（GB/月）</p>
                    <p><span class="labelRed">{{network.inbound}}</span>入站（GB/月）</p>
                    <p><span class="labelRed">{{network.outbound}}</span>出站（GB/月）</p>
                </td>
            </tr>
            <tr v-for="stro in storage">
                <td>{{stro.num}}</td>
                <td>存储</td>
                <td>
                    <p><span class="labelRed">{{stro.sna}}</span>共享存储（SAN）（GB）</p>
                    <p><span class="labelRed">{{stro.nsa}}</span>网络存储（NAS）（GB）</p>
                    <p><span class="labelRed">{{stro.cloudStorage}}</span>云存储（GB）</p>
                </td>
            </tr>
            <tr v-for="cdn in cdns">
                <td></td>
                <td>CDN</td>
                <td>
                    <p><span class="labelRed">{{cdn.cse.name}}</span>云厂商</p>
                    <p><span class="labelRed">{{cdn.bandwidth}}</span>带宽</p>
                    <p><span class="labelRed">{{cdn.startDate}}</span>购买开始时间</p>
                    <p><span class="labelRed">{{cdn.expireDate}}</span>购买结束时间</p>
                </td>
            </tr>
        </tbody>
    </table> -->
    <div class="compareResult-btn" style="margin-top:20px;">
        <button class="compare-btn compare-nextBtn" v-on:click="nextgo()">
            <span class="pl-10">下一步</span><i class="iconfont icon-xiayibu" style="margin-left:5px;"></i>
        </button>
        <button class="compare-prevBtn" v-on:click="prev()">
            <i class="iconfont icon-shangyibu1" style="margin-right:5px;"></i><span class="pr-5">上一步</span>
        </button>        
    </div>
    <div class="clear"></div>
</div>
</div>
</template>
<script>
import child from '../../../../components/steps/steps.vue'
import '../compareResult/compareResult.css'
export default{
    name:'compareResult',
    data(){
        return {
            compareResultList:[],
            resourceGroup:[],
            appId:'',
            queryType:'',
            appServer:[],
            dbServer:[],
            network:[],
            cdns:[],
            storage:[],
            details:[],
            confirm:[],
            length:'',
            res:false,
            pricelink:'',
            planSid:null,
            intentionSid:null,
            inserver:[]
        }
    },
    mounted:function(){
        this.queryType = this.$route.query.type;
        this.appId = this.$route.query.id;
        this.servied();
        this.getdata();
        this.getIntentionSid();
        // this.getfeature();
    },
    methods:{
        servied:function(){
            this.$this.get('/broker/plan/result/'+this.appId+'').then((response)=>{
                this.planSid = response.data.data.serverId;
            }).catch((error)=>{
            }) 
        },
        getIntentionSid:function(){
            this.$this.get('/broker/private/cloud/get/provider/'+this.appId+'').then((response)=>{
                if(response.data.code!=-1){
                    this.intentionSid = response.data.data.sid;
                    this.inserver.push(this.intentionSid);
                }
            }).catch((error)=>{
            })
        },
        intentionServer:function(sid,event){
            var el = event.currentTarget;
            var bool = !(el.checked);
            this.inserver.forEach(el =>{
                this.saveServer(true,el);
            });
            this.inserver = [];
            if(!bool){
                this.inserver.push(sid);
            }
            this.saveServer(bool,sid);
        },
        saveServer:function(bool,sid){
            let param = {
                "appid": this.appId,
                "del": bool,
                "matchType": 2,
                "sid": sid
            };
            this.$this.post('/broker/compare/save/intention',JSON.stringify(param));
        },
        getfeature:function(){
            let time = new Date();   
            this.$this.get('/broker/compare/selected/feature/'+this.appId+'?time='+time.getTime()).then((response)=>{
                this.details =  response.data.data;
                for(let variable  in this.details){   //variable 为属性名
                    this.confirm = this.details[variable][0].servers;
                }
                this.length = this.confirm.length+3;
            }).catch((error)=>{})
        },
        getdata:function(){
            this.$this.get('/broker/app/resource/group/'+this.appId+'').then((response)=>{
                if(response.data.data.appServer.length>0||response.data.data.dbServer.length>0||response.data.data.network!=null||response.data.data.storage.length>0||response.data.data.cdns.length>0){
                    this.res = true;
                }
                this.appServer = response.data.data.appServer;
                this.dbServer = response.data.data.dbServer;
                this.network = response.data.data.network;
                this.storage = response.data.data.storage;
                this.cdns = response.data.data.cdns;
            }).catch((error)=>{})
            let resultObj;
            if(this.$route.query.cloudId==undefined){
                resultObj = {
                    appid:this.appId,
                    searchAble:true,
                    sid:[]
                };                 
            }else{
               resultObj = {
                    appid:this.appId,
                    sid:this.$route.query.cloudId
                };
            }  
            let time = new Date();       
            this.$this.post('/broker/compare/result?time='+time.getTime(),JSON.stringify(resultObj)).then((response)=>{
                this.compareResultList = response.data.data.datas;
                this.getfeature();
            }).catch((error)=>{})
        },
        prev:function(){
            this.$router.push({path:'/compareQuestion',query:{id:this.appId,type:this.queryType}});
        },
        goBack:function(link){
            if(link=='comparelist'){
                this.$router.push({path:'/compareList'});
            }else if(link=='comparequestion'){
                this.$router.push({path:'/compareQuestion',query:{id:this.appId,type:this.queryType}});
            }
        },
        nextgo:function(){
            //this.$router.push({path:'/colligateReport',query:{id:this.appId,type:this.queryType}});
            this.$router.push({path:'/design',query:{id:this.appId,type:this.queryType}});
        }
    },
    components:{
        child
    }
}
</script>