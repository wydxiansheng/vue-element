<!--云规划-->
<template >
<div style="background:#eceef3" id="he">
      <div class="rightBs hideens">
            <ul>
                <li class="nexton" data-to="go1"></li>
                <li class="nextsec" data-to="go2"></li>
                
                <li class="nextcafe" data-to="go3"></li>
                <li class="nextf" data-to="go4"></li>
            </ul>
      </div>
         <!-- 悬浮框 -->
        <fixedbox></fixedbox>
    <div style="background:#f5f5f5;width:100%;height:70px;line-height:70px;" class="displayshow">
            <div class=" fixshow container">
                    <div class="col-md-3 col-xs-3"><a href="#ProductFeatures"><i class="iconfont icon-mn_gongneng"></i> 招募顾问计划</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#CoreStrengths"><i class="iconfont icon-shenpiliucheng"></i> 招募顾问合作流程</a></div>
                    <!--<div class="col-md-3 col-xs-3"><a href="#BigCafe"><i class="iconfont icon-woshou"></i> 已签约的大咖</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#QuickStart"><i class="iconfont icon-tuandui"></i> 加入大咖团队</a></div>-->
                    <!--<div class="col-md-3 col-xs-3"><a href="#sz"><i class="iconfont icon-shijianriqi"></i> 时间轴</a></div>-->
            </div>
    </div>
    <Sec active="2" class="sectb"></Sec>
    <div class="selecMain ">
            <div class="seleconeMain-banners  row ruset">
                 <div class="container">
                        <div class="seleconeMain-mainfir nfir col-xs-12 col-md-12" style="padding-left:50px">
                            <p class="selecone-pfir" style="font-weight:100;text-align:center;font-size:26px;color:#ffffff">赋能，聚力，生态，共赢</span></p>
                            <div class="seclone-dv">
                                <h3 class="selecone-pfir" style="font-weight:100;text-align:center;font-size:16px;color:#ffffff;line-height:26px">想让自己的IT圈和别人不同，也让他人的IT圈因自己不同，</br>
立即加入CloudBroker²的IT顾问圈，携手为他人、为企业、为行业赋能！</h3>
                            </div>
                             <p class="col-xs-12" style="margin-top:20px;margin-bottom:40px;text-align:center;padding:0 !important"><span class="spanTy" @click="lj">加入我们</span></p>
                        </div>
                 </div>
            </div>
            <div class="container naver">            
                <div class="" style="width:100%!important">
                    <div class="col-md-3 col-xs-3"><a href="#ProductFeatures" class="hoover-a"><i class="iconfont icon-mn_gongneng"></i> 招募顾问计划</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#CoreStrengths" class="hoover-a"><i class="iconfont icon-shenpiliucheng"></i> 招募顾问合作流程</a></div><!--
                    <div class="col-md-3 col-xs-3"><a href="#BigCafe" class="hoover-a"><i class="iconfont icon-woshou"></i> 已签约的大咖</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#QuickStart" class="hoover-a"><i class="iconfont icon-tuandui"></i> 加入大咖团队</a></div>-->
                </div>
            </div>
            <div class="nav-bottom-kk"></div>
            <div id="ProductFeatures" class="go1">
                <div class="container erfs whyContainer" style="margin-bottom:50px;">
                    <div class=" text-left redtitle">
                       <span class="redLine"></span><span class="redlasttitle">招募顾问计划</span>
                    </div>
                    <div class="row text-left" style="margin-left:10px !important;font-size:14px;color:#666666;line-height:30px;">我们致力于打造新型的云服务管理MSP+模式，帮助企业、顾问和服务商之间建立起稳定的合作关系，为三方创建开放的、公平的、专业的第三方服务平台。CloudBroker²同他的成长历程一样，始终尊重宝贵的顾问资源，并与之共同成长，携手建设新型的顾问服务生态圈，共同提供集顾问的第三方培训、咨询和                   技术服务的为一体的全新生态圈。
                    </div>
                 </div>
            </div>
            <div style="width:100%;background:#f8f8f8" id="CoreStrengths" class="go2">
            <div class="container  erfs" style="padding-top:20px;padding-bottom:50px">
                <div class=" text-left redtitle">
                    <span class="redLine"></span><span class="redlasttitle">招募顾问合作流程</span>
                </div>
                <div class="col-xs-12 cla text-center">
                     <img src="../../../assets/er-icon/zhaomu.png" alt="" style="position:relative">   
                     <span style="position:absolute;left:7.2%;bottom:-20px;color:#333333;" class="positionSpans positionSpans1">在线咨询</span>
                     <span style="position:absolute;left:34%;bottom:-20px;color:#333333;" class="positionSpans positionSpans2">准备材料</span>
                     <span style="position:absolute;left:61.2%;bottom:-20px;color:#333333;" class="positionSpans positionSpans3">线下洽谈</span>
                     <span style="position:absolute;right:5.6%;bottom:-20px;color:#333333;" class="positionSpans positionSpans4">最终通过</span>
                </div>
                <div class="col-xs-12 text-left" style="margin-top:70px;padding-left:7%;">
                    <div class="zhaomu">招募规则备注：</div>
                    <div class="zhaomu1 zhaomu2"><span>1、在线咨询</span> 点击右面悬浮窗口，进入“Pro. 吴” 或拨打 400-828-7308。</div>
                    <div class="zhaomu1"><span>2、准备材料</span> 个人介绍、文档实例介绍、联系电话、EMALL、期望合作模式。</div>
                    <div class="zhaomu1"><span>3、申请规则</span> 合作伙伴活动最终解释权归京玉所有。</div>
                </div>
            </div>
            </div>
            <!--  -->
            <div class="container  erfs">
            <div class="go3" style="padding-top:20px;" id="BigCafe">
                <div class=" text-left redtitle">
                    <span class="redLine"></span><span class="redlasttitle">已签约的大咖</span>
                </div>
                <div class="row">
                    <div class="col-md-4" v-for="item in cafelist" v-on:click="teamdetail(item.userProfessor.id)">
                        <div class="bigcafe-desc-list resruit-cafe" style="height:220px;">
                            <img :src="item.userProfessor.headRoundImg" alt="">
                            <div class="bigcafe-desc-name">{{item.realname}}</div>
                            <div class="bigcafe-desc-jobs">{{item.userProfessor.title}}</div>
                        </div>
                    </div>
                </div>
            </div>
            </div>
            <!--  -->
           <!-- <div style="width:100%; background: rgb(248, 248, 248); margin-top: 50px;" id="QuickStart" class="go4">
                <div class="seleconeMain-shrts container erfs " style="padding-top:20px;padding-bottom:40px" >
                    <div class=" text-left redtitle">
                       <span class="redLine"></span><span class="redlasttitle">加入大咖团队</span>
                    </div>
                    <div class="col-md-6 text-left iuols col-xs-12">
                        <div><input type="text" placeholder="姓名" v-model="names"></div>
                        <div><input type="text" placeholder="联系电话" v-model="phones"></div>
                        <div class="inpusa"><input type="text" placeholder="请输入短信验证码" v-model="dx" ><div class="dvsa" @click="hyDemo">获取验证码</div></div>
                        <div><input type="text" placeholder="公司名称" v-model="gs"></div>

                        <div>
                            <select name="" id="" v-model="hys">
                                <option value="">选择行业</option>
                                <option :value="ins.id" v-for="ins in resulters">{{ins.name}}</option>
                            </select>
                        </div>
                        
                        <div class="welecone"><span @click="wle" class="welecone-span">{{haha}}</span></div>
                        
                    </div>
                    <div class="col-md-6 col-xs-12">
                        <div class="text-left rightDiv">
                            <div class="rightDiv-child">
                                <div style=" font-size:14px;color:#000;"><i class="iconfont icon-tishi" style="color:#da121a"></i> 温馨提示：</div>
                                <div class="rightDiv-child-S" style="margin-top:10px;">点击右面悬浮窗口，进入“Pro. 吴”或拨打 400-828-7308</div>
                                <div class="rightDiv-child-S">可随时和我们联系。</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>-->
       
           
      
            <div style="background:#ededed;;width:100%;height:auto;">
                <div class="seleconeMain-footer">
                    <div class="container text-left" style="width:60%;padding-left:cd30px;">
                            <div class="col-md-3 col-xs-12" style="margin-top:27px;margin-bottom:20px;"><img src="../../../assets/qian.png" alt="" style="width:18%;margin-right:10px"><span style="font-size:14px;color:#333333">专注专业化服务</span></div>
                            <div class="col-md-3 col-xs-12 juzhong " style="margin-top:27px;margin-bottom:20px;"><img src="../../../assets/24fuwu.png" alt="" style="width:18%;margin-right:10px"><span style="font-size:14px;color:#333333">7×24小时顾问支持</span></div>
                            <div class="col-md-3 col-xs-12 juzhong " style="margin-top:27px;margin-bottom:20px;"><img src="../../../assets/1fuwu.png" alt="" style="width:18%;margin-right:10px;" class="imgeys"><span style="font-size:14px;color:#333333">1V1顾问咨询服务</span></div>
                            <div class="col-md-3 col-xs-12 juright" style="margin-top:27px;margin-bottom:20px;padding-right:40px !important;"><img src="../../../assets/90fuwu.png" alt="" style="width:22%;margin-right:10px"><span style="font-size:14px;color:#333333">90秒极速响应</span></div>
                    </div>
                </div>
            </div>
    </div>
    <Sex></Sex>
</div>


</template>
<style>
/**/
.resruit-cafe{
    border-bottom:2px #da121a solid;
}
.dvsa:hover{
    background:#EF131D;
}
.welecone-span:hover{
     background:#EF131D;
}
.dvsa:hover{
    cursor:pointer;
}
.ruset{
    background:url("../../../assets/er-icon/bannert.png") no-repeat;
    text-align:center;background-size:100% 100%;
   
}
.dv2:hover{
    cursor:pointer;
}

.welecone span{
    background:#da121a;
    border-radius:4px;
    width:129px;
    height:32px;
    line-height:32px;
    color:#fff;
    text-align:center;
    display:inline-block;
}
.welecone span:hover{
    cursor:pointer;
}

.rightDiv .rightDiv-child{
    padding:20px 30px;
}
.rightDiv-child-S{
     font-size:14px;
    color:#999;
    line-height:30px;
}
.zhaomu{
    font-size:14px;
    color:#333333;
}
.zhaomu1{
    font-size:12px;
    color:#333333;
    line-height:30px;
}
.zhaomu2{
    margin-top:10px;
}
.zhaomu1 span{
    color:#000;
}
.naver i{
    color:#c2c2c2;
}
.fixshow i{
    color:#c2c2c2;
}
/**/
.rightBs ul li{
    background:#d8d8d8;
    width:10px;
    height:10px;
    border-radius:100%;
   margin-bottom:10px;
}
.rightBs ul li a{
    width:10px;
    height:10px;
    border-radius:100%;
    display:inline-block;
}
.rightBs ul{
    position:fixed;
    right:20px;
    top:40%;
}
.timeli,.timeli1,.timeli2,.timeli3,.timeli4{
    font-size:14px;
    color:#e41e2b;
}
.timeli{
     position:absolute;
    top:-45px;
    left:15%;
}
.timeli1{
     position:absolute;
    top:-45px;
    left:32%;
}
.timeli2{
     position:absolute;
    top:-45px;
    left:49%;
}
.timeli3{
     position:absolute;
    top:-45px;
    left:66%;
}
.timeli4{
     position:absolute;
    top:-45px;
    left:83%;
}
.licheng,.licheng1,.licheng2,.licheng3,.licheng4{
    font-size:14px;
    color:#666666;
}
.licheng{
       position:absolute;
        top:45px;
        left:10%;
}
.licheng1{
       position:absolute;
        top:45px;
        left:27%;
}

.licheng2{
       position:absolute;
        top:45px;
        left:46%;
}

.licheng3{
       position:absolute;
        top:45px;
        left:61%;
}
.licheng4{
       position:absolute;
        top:45px;
        left:80%;
}
.gh{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    top:-10px;
    left:-2px;
}
.gq{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:17%;
    top:-10px;
}
.gw{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:34%;
    top:-10px;
}
.ge{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:51%;
    top:-10px;
}
.gr{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:68%;
    top:-10px;
}
.gt{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:85%;
    top:-10px;
}
.gy{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:100%;
    top:-10px;
}
.gh div{
    background:#ffffff;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gq div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gw div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.ge div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gr div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gt div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gy div{
    background:#fff;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
@media (max-width: 768px) {
      .juright,.juzhong{
          text-align:left !important;
      }
    .inpusa{
        position:relative;
        width:257px;
    }
    .dvsa{
        width:100px;height:32px;line-height:32px;text-align:center;background:#da121a;color:#fff;border-radius:4px;position:absolute;
        right:5px;top:5px;
    }
    .el-message-box{
        width:274px !important;
    }
     .positionSpans{
        font-size:12px;
      }
      .positionSpans1{
          left:3.2% !important;
      }
      .positionSpans2{
          left:33.2% !important;
      }
      .positionSpans3{
        left:58% !important;
      }
      .positionSpans4{
          right:1.6% !important;
      }
      .ljs{
            width:100%;
            display:inline-block;
            margin-bottom:10px;
        }
        .imgets{
            display:none;
        }
        .cla img{
            width:100%;
        }
        .rightDiv{
            margin-top:20px;
            border:1px solid #dedede;
            border-radius:4px;
            width:220px;
            height:220px;   
        }
        .iuols input,.iuols select{
            margin-bottom:20px;
            padding-left:20px;
            border:1px solid #dedede;
            border-radius:4px;
            width:257px !important;
            height:40px !important;
        }
}
@media (min-width: 768px) {
    .juright{
        text-align:right;
    }
    .juzhong{
        text-align:center;
    }
    .inpusa{
        position:relative;
        width:407px;
    }
    .dvsa{
        width:100px;height:32px;line-height:32px;text-align:center;background:#da121a;color:#fff;border-radius:4px;position:absolute;
        right:5px;top:5px;
    }
    .positionSpans{
        font-size:16px;
    }
    .color_999{
        line-height:20px !important;
    }
      .ljs{
            width:16%;
            display:inline-block;
        }
     .imgets{
          display:inline-block;
     }
     .rightDiv{
        border:1px solid #dedede;
        border-radius:4px;
        width:457px;
        height:280px;   
    }
    .iuols input,.iuols select{
        margin-bottom:20px;
        padding-left:20px;
        border:1px solid #dedede;
        border-radius:4px;
        width:407px !important;
        height:40px !important;
    }
}
.mainPds{
    line-height:20px;
}
.crounds{
    background:#f5f5f5;
    border-radius:100px;
    width:88px;
    height:85px;
    margin:0 auto;
    line-height:80px;
}
.fixshow a{
    font-size:14px;
    color:#333333;
}
.fixshow a:hover{
    font-size:14px;
    color:#da121a;
    border-bottom:1px solid #da121a;
    padding-bottom:20px;
}
.fixshow i:hover{
    font-size:14px;
    color:#da121a;
    border-bottom:1px solid #da121a;
    padding-bottom:20px;
}
.displayshow{
    display:none;
    position:fixed;
    top:0;
    z-index:999999999;
}
.cround{
    background: #f5f5f5;
    border-radius:100%;
    width:100px;
    height:130px;
    margin:0 auto;
    line-height:130px
}
.erfs{
        max-width: 1020px !important;
}
.redtitle{
    margin:40px 0 40px 0;
}
.redLine{
    background: #da121a;
    width: 3px;
    height: 25px;
    float: left;
    margin-right: 10px;
    margin-top: 2px;
}
.redlasttitle{
    font-size:20px;
    color:#2b2b2b;
}
.sectb{
    display:block
}
.selecMain{
    background:#fff;
}
.naver{
    height:70px;
    line-height:70px;
}
.naver a{
    font-size:14px;
    color:#333333;  
}
.naver a i{
    font-size:14px;
    color:#A5A5A5;  
}
.naver a:hover{
    cursor:pointer;
    color:#da121a;
    display:inline-block;
    border-bottom:1px solid #da121a;
}
.naver a i:hover{
    cursor:pointer;
    color:#da121a;
    display:inline-block;
    border-bottom:1px solid #da121a;
}
.nav-bottom-kk{
    width:100%;
    height:1px;
    background:#d6d6d6
}
.mt{
    margin-top:20px;
}
.h2-18{
    font-size:18px !important
}
.bigFang{
    display:inline-block;   
    background:#fdfdfd;
    border:1px solid #f0f0f0;
    box-shadow:0 0 1px 2px rgba(236,236,236,0.50);
    border-radius:2px;
    width:100%;
    height:80px;
    font-size:12px;
    text-align:left;
    position:relative;
}
.bigimg{
    display:inline-block;
    line-height:80px;
    width:40px
}
.dv1{
    font-size:14px;
    color:#2b2b2b;
    margin-top:10px;
    margin-left:5px;
}
.dv2{
    font-size:12px;
    color:#d5272c;
    margin-left:5px;
    margin-top:10px;
}
.dv3{
    font-size:48px;
    color:#da121a;
    position:absolute;
    right:10px;bottom:-10px;
}
.liHoversBj:hover{
    background:#EF131D;
}
.timezhou{
    border:2px solid #d2d2d2;
    width:90%;
    margin:0 auto 90px auto;
    height:0px;
    position:relative;
}
@media (min-width: 768px) {
    .lasilasis{
          margin-top:190px;
    }
    .seleconeMain-mainfir{
        margin-bottom:50px;
    }
    .imgeys{
        margin-left:20px !important
    }
}
@media (max-width: 768px) {
    .hideens{
        display:none;
    }
    .lasilasis{
        margin-top:10px;
        margin-bottom:20px;
    }
    .imgeys{
        margin-left:0px !important
    }
    .seleconeMain-mainfir{
        margin-bottom:0px;
    }
    .naver  div{
            overflow: hidden;
            white-space: nowrap;
            text-overflow: ellipsis;
        }
        .fixshow div{
            overflow: hidden;
            white-space: nowrap;
            text-overflow: ellipsis;
        }
}
   .container{
     
        max-width: 1090px;

   }
  .seleconeMain-shrts h4{
       font-weight:100;
   }
   .seleconeMain-echarts h4{
       font-weight:100;
   }
   .footer-laster{
       
       margin-top:20px;
   }
   dl .dts{
        float:left;
        margin-top:10px;
        margin-right:10px;
   }
   dl .dds{
       text-align:left;
   }
   .dds-li{
       font-size:14px;
       color:#333333;
   }
   .dds-lis{
       font-size:12px;
       color:#666666;
       margin-top:5px;
   }
   *{margin:0px;padding:0px;}
   

   .seleconeMain-mainfir{margin-top:160px;}
   .nfir{margin-bottom:48px}
   .seleconeMain-mainfir .selecone-pfir{
        font-size:26px;
        color:#ffffff;
        text-align:center;
   }
   .seleconeMain-mainfir .selecone-pfir span{
       font-weight:100;
       color:#ccc;
   }
  
   .seclone-dv p{
       font-size:14px;
       color:#fff;
       text-align:center;
   }
   .seleconeMain-charts{
       width:100%;
   }
   .seleconeMain-charts H4{
       font-size:26px;
       color:#333333;
       text-align:center;
   }
   .seleconeMain-charts .h4Fir{
         margin-top:50px;
   }
   .Main-ul li img{
       width:47px;
       height:47px;
   }
   .seleconeMain-charts .h4Firer{
       margin-top:10px;
       margin-bottom:20px;
   }
   .seleconeMain-echarts .shrts-h4{
       margin-top: 40px;
           font-size: 26px;
    color: #333333;
    text-align: center;
   }
   .seleconeMain-echarts .shrts-h4er{
       margin-top: 10px;
    margin-bottom: 20px;
        font-size: 26px;
    color: rgb(51, 51, 51);
    text-align: center;
    }
   .seleconeMain-charts p{
       font-size:16px;
       color:#777777;
       text-align:center;
   }
   .seleconeMain-img img{
       width:42%;
       height:42%;
       
   }
   .seleconeMain-img{
       margin-top:25px;
       margin-bottom:60px;
   }
   .seleconeMain-shrts h4{
       font-size:26px;
       color:#333333;
       text-align:center;
     
   }
   .seleconeMain-shrts .shrts-h4{
      margin-top:50px;
   }
   .seleconeMain-shrts .shrts-h4er{
       margin-top:10px;
       margin-bottom:20px;
   }
   .seleconeMain-shrts p{
       font-size:16px;
       color:#777777;
       text-align:center;  
   }
   .seleconeMain-simg{
        margin-top:25px;
       margin-bottom:60px;
   }
   .seleconeMain-simg img{
       width:80%;
       height:80%;
   }
   .Main-ul{
       padding-left:20px;
   }
   .Main-li{
       margin-top:20px;
   }
   .iconer-img{
       margin-right:15px;
   }
   .seleconeMain-simg ul li .sp4{
       font-size:14px;
       color:#666666;
       text-align:center;
   }
   .seleconeMain-simg ul li .sp1{
      background:#e41e2b;
      width:20px;font-size:16px;
      height:20px;
      text-align:center;
      display:inline-block;
      border-radius:100%;
      color:#fff;
   }
   .seleconeMain-simg ul li .sp2{
     background:#e15f2d;
      width:20px;font-size:16px;
      height:20px;
      text-align:center;
      display:inline-block;
      border-radius:100%;
      color:#fff;
   }
   .seleconeMain-simg ul li .sp3{
     background:#f7a72c;
      width:20px;font-size:16px;
      height:20px;
      text-align:center;
      display:inline-block;
      border-radius:100%;
      color:#fff;
   }
    .seleconeMain-simg ul{
        margin-top:20px;
    }
     .seleconeMain-simg ul li span{
         margin-right:5px;
     }
    .seleconeMain-simg ul li{
        margin-bottom:10px;
    }
    .seleconeMain-echarts p{
    font-size: 16px;
    color: rgb(119, 119, 119);
    text-align: center;
    }
    .seleconeMain-echarts .child-p{
        font-size:26px;
       color:#333333;
       text-align:center;
       margin-top:50px; 
    }
    .seleconeMain-echarts .child-ps{
           font-size:26px;
       color:#333333;
       text-align:center;
    }
    .seleconeMain-echarts .child-pl{
           font-size:16px;
       color:#333333;
       text-align:center;
    }
    .spanTy{
        border:1px solid #e41e2b;font-size:12px;color:#fff;padding:10px 25px;display:inline-block;text-align:center;background:#e41e2b;margin-right:10px;
    }
    .panTy{
        border:1px solid #f0f0f0;font-size:12px;color:#f0f0f0;padding:10px 25px;display:inline-block;text-align:center;
    }
    .panTy:hover{
        color:#da121a;
        background:#fff;
        cursor:pointer;
    }
    .spanTy:hover{
        cursor:pointer;
        background:#fff;
        color:#e41e2b;
        border:1px solid #fff;
    }
     .scrollUp:hover{
        cursor:pointer;
    } 
</style>
<script>
    $(document).ready(function(){ 
                        // $(".rightBs ul li").find("a").click(function(){
                        //     // $(".rightBs ul li").css("background","#d8d8d8");
                        //     // $(this).css("background","#da121a");
                        //     alert(1)
                        // });
                       $(".fixshow a").hover(function(){
                                $(this).find("i").css("color","#da121a")
                        },function(){
                                $(this).find("i").css("color","#c2c2c2")
                        })
                        $(".naver a").hover(function(){
                                $(this).find("i").css("color","#da121a")
                        },function(){
                                $(this).find("i").css("color","#c2c2c2")
                        })
                     $(window).scroll(function(){
                    // console.log($(this).scrollTop());
                        // console.log("p",$(".naver").offset().top - $(window).scrollTop())
                        // console.log($(window).scrollTop())
                        // if($(this).scrollTop()>80){
                        //     $(".sectb").css("display","none");
                        // };
                        // if($(this).scrollTop()<80){
                        //     $(".sectb").css("display","block");
                          
                        // };
                         if($(".naver").length==1){
                          
                            var topa = $(".naver").offset().top - $(window).scrollTop();
                             if(topa<0){
                                 $(".displayshow").css("display","block") 
                             }else if(topa>0){
                                  $(".displayshow").css("display","none") 
                                  $(".rightBs ul li").css("background","#d8d8d8") 
                             }
                            // console.log($("#ProductFeatures").offset().top - $(window).scrollTop());
                             if($(window).scrollTop()+70>=$("#ProductFeatures").offset().top){
                                $(".rightBs ul li").css("background","#d8d8d8") 
                                $(".nexton").css("background","#da121a")
                             }
                             if($(window).scrollTop()+70>=$("#CoreStrengths").offset().top){
                                  $(".rightBs ul li").css("background","#d8d8d8") 
                                    $(".nextsec").css("background","#da121a")
                             }
                             
                             if($("#BigCafe").length>0){
                                if($(window).scrollTop()+70>=$("#BigCafe").offset().top){
                                    $(".rightBs ul li").css("background","#d8d8d8") 
                                        $(".nextcafe").css("background","#da121a")
                                }
                            }
                            if($("#QuickStart").length>0){
                                if($(window).scrollTop()+70>=$("#QuickStart").offset().top){
                                    $(".rightBs ul li").css("background","#d8d8d8") 
                                        $(".nextthe").css("background","#da121a")
                                }
                            }
                             if($("#he").height()-($(window).height()+$(this).scrollTop())<50){
                                 $(".rightBs ul li").css("background","#d8d8d8");
                                  $(".nextf").css("background","#da121a")  
                             }
                        }
                    });
            
                    


              })
 import Sec from "../../../components/SecondaryPages/SecondaryPages.vue"
 import Sex from "../../../components/SecondaryPages/SecondaryFooter.vue"
 import fixedbox from '../../../components/SecondaryPages/protalFixed.vue';
    export default{
         name: 'cloudplanning',
        components:{
            Sec,
            Sex,
            fixedbox
        },
        data(){
            return{
                 resulters:[],
                 names:"",
                 phones:"",
                 gs:"",
                 hys:"",
                 dx:"",
                 haha:"欢迎加入我们",
                 cafelist:[]
            }
        },}
       /* methods:{
            teamdetail:function(cafeid){
                this.$router.push({path:'/teamDetail',query:{bigcafeId:cafeid}});
            },
            getlist:function(){
                this.$this.get('/broker/prof/getList').then((response)=>{
                    //console.log('---',response.data);
                    this.cafelist = response.data.data;
                }).catch((error)=>{
                })
            },
              ctaCloundCsbs:function(){
                    window.open("http://demo.csb-china.com")
                },
            spanTy:function(){
                this.$router.push({path: '/login'});
            },
            lj:function(){
                this.$router.push({path: '/registerOne'});
            },
            hyDemo:function(){
                 if(this.phones!=""){
                     var oas = {
                            "mobile":this.phones,
                            "username":this.names,
                            }
                     this.$this.post('/broker/sms/send/code/experts',oas).then((pon)=>{  //获取验证码
                                                                
                                   
                                }).catch((error)=>{
                    })
                 }else{
                   return false;
                 }
            },
            wle:function(){
               if(this.names==""||this.phones==""||this.gs==""||this.hys==""||this.dx==""){
                   this.$alert('请完善您的信息，谢谢！', '提示', {
                    confirmButtonText: '我知道了',
                    confirmButtonClass:'lay-btn-red',
                     showClose:false,
                    type: 'warning',
                    }).then(() => {
                        
                    }).catch(() => {
                        
                    });
               }else{
                   var obj = {
                        "company":this.gs,
                        "industryId":this.hys,
                        "name":this.names,
                        "tel": this.phones,
                        "type": 1
                   }
                    let strObj = JSON.stringify(obj);
                    this.$this.post('/broker/portal/join/us/'+this.dx,strObj).then((pon)=>{  //获取消息类型
                                //this.scsss = pon.data.msg
                                        this.$alert('留言成功，我们会尽快与您联系。', '温馨提示', {
                                        confirmButtonText: '我知道了',
                                        showClose:false,
                                        confirmButtonClass:'lay-btn-red',
                                        type: 'warning'
                                    });
                                    this.hys = "";
                                    this.names = "";
                                    this.phones = "";
                                    this.gs = "";
                                    this.dx = "";
                                }).catch((error)=>{
                    })
               }
            }
        },*/
      /*  mounted:function(){
            this.getlist();
               $(".rightBs ul li").click(function(e){
                               //$(".rightBs ul li").css("background","#d8d8d8");
                               var s = $(this).index();
                               //console.log(s)
                             $(".rightBs ul li").not($(this)).css("background","#d8d8d8")
                             $(this).css("background","#da121a")
                             var target = e.target;
                             var id = $(target).data("to");
                             $('html,body').animate({scrollTop:$('.'+id).offset().top+90}, 800);
                            
                         
                })

                this.$this.get('/broker/prop/industry/').then((pon)=>{  //获取消息类型
                                   
                                    this.resulters = pon.data.data;
                                                               
                }).catch((error)=>{
                    console.log("失败")
                })
            
        }*/
    //     mounted:function(){
    //         $(document).ready(function(){ 
    //                    $.fn.extend({
    //                     animateCss: function (animationName) {
    //                         var animationEnd = 'webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend';
    //                         $(this).addClass('animated ' + animationName).one(animationEnd, function() {
    //                         $(this).removeClass('animated ' + animationName);
    //                         });
    //                     }           
    //                 });
    //          var index=0;
    //          var isn = true;
    //          $(window).scroll(function(){
              
    //            if(isn==true){
    //                 if($(this).scrollTop()>300&&$(this).scrollTop()<450){
    //                   $(".seleconeMain-charts").animateCss('bounceInLeft');
    //                 };
    //                 if($(this).scrollTop()>800&&$(this).scrollTop()<850){
    //                     $(".seleconeMain-shrts").animateCss('bounceInLeft');
    //                 };
    //                 if($(this).scrollTop()>1300&&$(this).scrollTop()<1350){
    //                     $(".broundDow").animateCss('bounceInLeft');
    //                 };
    //                 if($(this).scrollTop()>1750&&$(this).scrollTop()<1800){
    //                     $(".broundU").animateCss('bounceInLeft');
    //                     index=1;
    //                 };
    //            }
    //             if(index==1){
    //                isn = false;
    //            }
                  
    //     })
             
               
    //     })
    // }
  //  }
</script>
