<!--云规划-->
<template >
<div style="background:#eceef3" id="he">
      <div class="rightBs hideens">
            <ul>
                <li class="nexton" data-to="go1"></li>
                <li class="nextsec" data-to="go2"></li>
                <li class="nextthe" data-to="go3"></li>
                <li class="nextf  hideens" data-to="go4"></li>
            </ul>
      </div>
     <!-- 悬浮框 -->
    <fixedbox></fixedbox> 
    <div style="background:#f5f5f5;width:100%;height:70px;line-height:70px;" class="displayshow">
            <div class=" fixshow container">
                    <div class="col-md-3 col-xs-3"><a href="#ProductFeatures"><i class="iconfont icon-mn_gongneng"></i> 产品功能</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#CoreStrengths"><i class="iconfont icon-hexin"></i> 核心优势</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#QuickStart"><i class="iconfont icon-feiji"></i> 快速入门</a></div>
                    <div class="col-md-3 col-xs-3 hideens"><a href="#TheTimeline"><i class="iconfont icon-shijianriqi"></i> 时间轴</a></div>
            </div>
    </div>
    <Sec active="1" class="sectb"></Sec>
    <div class="selecMain ">
            <div class="seleconeMain-banners selectHelp row ">
                 <div class="container">
                        <div class="seleconeMain-mainfir nfir col-xs-12 col-md-6" style="padding-left:50px">
                            <p class="selecone-pfir" style="font-weight:100;text-align:left;font-size:26px;color:#f6f6f6">场景化、智能化、专业化</span></p>
                            <div class="seclone-dv">
                                <p style="font-weight:100;text-align:left;font-size:16px;color:#f2f2f2;line-height:26px;">借助大数据和AI技术，只需导入资源，一键智能完成云推荐配置和设计拓扑，助您省时和省钱！</p>
                            </div>
                             <p class="col-xs-12" style="margin-top:20px;margin-bottom:40px;text-align:left;padding:0 !important"><span class="spanTy" @click="lj">立即注册</span><span class="panTy" @click="ctaCloundCsbs()">DEMO体验</span></p>
                        </div>
                        <div class="col-md-6 col-xs-12 text-left lastus"><img src="../../../assets/ii2@1x.png" alt="" style="float: right;width:85%"></div>
                 </div>
            </div>
            <div class="container naver">            
                <div class="row">
                    <div class="col-md-3 col-xs-3"><a href="#ProductFeatures" class="hoover-a"><i class="iconfont icon-mn_gongneng"></i> 产品功能</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#CoreStrengths" class="hoover-a"><i class="iconfont icon-hexin"></i> 核心优势</a></div>
                    <div class="col-md-3 col-xs-3"><a href="#QuickStart" class="hoover-a"><i class="iconfont icon-feiji"></i> 快速入门</a></div>
                    <div class="col-md-3 col-xs-3 hideens"><a href="#TheTimeline" class="hoover-a"><i class="iconfont icon-shijianriqi"></i> 时间轴</a></div>
                </div>
            </div>
            <div class="nav-bottom-kk"></div>
            <div id="ProductFeatures" class="go1">
                <div class="container erfs whyContainer" style="margin-bottom:50px;">
                    <div class=" text-left redtitle">
                       <span class="redLine"></span><span class="redlasttitle">产品功能</span>
                    </div>
                    <div class="row text-center">
                        <div class="col-xs-12 col-sm-3 blurb-cta">
                            <div class="crounds"><img src="../../../assets/k.png" alt="" class="Yunimg"></div>
                            <h2 class="h2-18">推荐配置规格</h2>
                            <div class="bluar-ccc mt">
                                <p class="text-center"><span class="color_999 text-center" style="font-size:14px;color:#666666;">云分析对象资源导入后，一键生成推荐云规格配置；同时提供手动修正功能。</span></p>
                            </div>
                        </div>
                        <div class="col-xs-12 col-sm-3 blurb-cta">
                            <div class="crounds"><img src="../../../assets/j.png" alt="" class="Yunimg"></div>
                            <h2 class="h2-18">自动化拓扑</h2>
                            <div class="bluar-ccc mt">
                                <p class="text-center"><span class="color_999 text-center" style="font-size:14px;color:#666666;">支持交互式的自动化拓扑设计，用户可根据实际需求进行优化。</span></p>
                            </div>
                        </div>
                        <div class="col-xs-12 col-sm-3 blurb-cta">
                            <div class="crounds"><img src="../../../assets/i.png" alt="" class="Yunimg"></div>
                            <h2 class="h2-18">多云厂商价格优选</h2>
                            <div class="bluar-ccc mt">
                                <p class="text-center"><span class="color_999 text-center" style="font-size:14px;color:#666666;">支持阿里云、腾讯云、华为云、Azure等厂商在线价格比较，借助TOP排名和星级评定助用户优选。</span></p>
                            </div>
                        </div>
                         <div class="col-xs-12 col-sm-3 blurb-cta">
                            <div class="crounds"><img src="../../../assets/h.png" alt="" class="Yunimg"></div>
                            <h2 class="h2-18">星级评定</h2>
                            <div class="bluar-ccc mt">
                                <p class="text-center"><span class="color_999 text-center" style="font-size:14px;color:#666666;">提供独立、公开、透明的价格和云厂商两个维度的星级评定。</span></p>
                            </div>
                        </div>
                    </div>
                 </div>
            </div>
            <div style="width:100%;background:#f8f8f8" id="CoreStrengths" class="go2">
            <div class="container  erfs" style="padding-top:20px;padding-bottom:20px">
                <div class=" text-left redtitle">
                    <span class="redLine"></span><span class="redlasttitle">核心优势</span>
                </div>
                <div class="col-xs-12 cla text-left">
                <div class="col-xs-12 col-sm-6 claes " style="padding-left:1px;">
                    <dl>
                        <dt style="float:left;margin-right:20px;margin-left:10px;"><img src="../../../assets/2222222.png" alt="" class="tranImg"></dt>
                        <dd style="diaplay:inline-block;">
                            <div class="mainpa text-left">
                                <p style="padding-top:6px;font-size:18px;color:#333333;">科学化</pstyle>
                                <p class="mainPds">汇集数万个工作负载画像，结合AI学习， 云方案设计越来越准确和科学。</p>
                            </div>
                        </dd>
                    </dl>
                </div>
                <div class="col-xs-12 col-sm-6 claes" style="padding-left:1px;">
                    <dl>
                        <dt style="float:left;margin-right:20px;margin-left:10px;"><img src="../../../assets/3333.png" alt="" class="tranImg"></dt>
                        <dd style="diaplay:inline-block">
                            <div class="mainpa text-left">
                                <p style="padding-top:6px;font-size:18px;color:#333333;">低成本化</pstyle>
                                <p class="mainPds">3分钟内完成多个云厂商实例价格优选，5分钟内完成购买实例下单，简化上云难度，实现降本增效。</p>
                            </div>
                        </dd>
                    </dl>
                </div>
                <div class="col-xs-12 col-sm-6 claes" style="padding-left:1px;">
                    <dl>
                        <dt style="float:left;margin-right:20px;margin-left:10px;"><img src="../../../assets/444.png" alt="" class="tranImg"></dt>
                        <dd style="diaplay:inline-block">
                            <div class="mainpa text-left">
                                <p style="padding-top:6px;font-size:18px;color:#333333;">便捷化</pstyle>
                                <p class="mainPds">一键导入资源，一键完成云方案设计，一键生成云分析综合报告。</p>
                            </div>
                        </dd>
                    </dl>
                </div>
                <div class="col-xs-12 col-sm-6 claes" style="padding-left:1px;">
                    <dl>
                        <dt style="float:left;margin-right:20px;margin-left:10px;"><img src="../../../assets/66666.png" alt="" class="tranImg"></dt>
                        <dd style="diaplay:inline-block">
                            <div class="mainpa text-left">
                                <p style="padding-top:6px;font-size:18px;color:#333333;">可视化</pstyle>
                                <p class="mainPds">交互式的图表设计，直观的、便捷的展现了上云方案设计和多云价格优选过程。</p>
                            </div>
                        </dd>
                    </dl>
                </div>
                
                </div>
            </div>
            </div>
            <div style="width:100%;" id="QuickStart" class="go3">
                <div class="seleconeMain-shrts container erfs " style="padding-top:20px;padding-bottom:20px" >
                    <div class=" text-left redtitle">
                       <span class="redLine"></span><span class="redlasttitle">快速入门</span>
                    </div>
                    <div style="text-align:left;">
                        <div class="ljs iks">
                            <div class="bigFang ">
                                <div class="dv1">注册／登录</div>
                                <div class="dv2" @click="spanTy">立即体验 > </div>
                                <div class="dv3">1</div>
                            </div>
                        </div>
                        <div class="imgets ik"><img src="../../../assets/line.png" alt="" class="bigimg1 bigimg"></div>
                        <div class="ljs">
                            <div class="bigFang">
                                <div class="dv1">云设计／自动化拓扑</div>
                                <div class="dv2" @click="spanTy">立即体验 > </div>
                                <div class="dv3">2</div>
                            </div>
                        </div>
                        <div class="imgets ik"><img src="../../../assets/line.png" alt="" class="bigimg2 bigimg"></div>
                        <div class="ljs">
                            <div class="bigFang">
                                <div class="dv1">云设计／价格优选</div>
                                <div class="dv2" @click="spanTy">立即体验 > </div>
                                <div class="dv3">3</div>
                            </div>
                        </div>
                        <div class="imgets ik"> <img src="../../../assets/line.png" alt="" class="bigimg3 bigimg"></div>
                        <div class="  ljs">
                           <div class="bigFang">    
                                <div class="dv1">云设计／购买</div>
                                <div class="dv2" @click="spanTy">立即体验 > </div>
                                <div class="dv3">4</div>
                           </div>
                        </div>
                        
                        <div class="col-md-12 seleconeMain-img" style="margin-top:72px;">
                            <div class="col-md-12 col-xs-12 text-center"><img src="../../../assets/tuopu.png" alt="" class="tuopus"></div>
                        </div>
                    </div>
                </div>
            </div>
       
             <div style="background:#f8f8f8;width:100%" id="TheTimeline" class="go4  hideens">
                <div class="seleconeMain-echarts container broundU erfs">
                     <div class=" text-left redtitle">
                       <span class="redLine"></span><span class="redlasttitle">时间轴</span>
                    </div>
                    <div class="col-md-12 seleconeMain-img" >
                       <div class="timezhou">
                            <div class="ga"><div></div></div>
                            <div class="gs"><div></div></div>
                            <div class="gd"><div></div></div>
                            <div class="gf"><div></div></div>
                            <div class="gg"><div></div></div>
                            <div class="gm"><div></div></div>
                            <div class="gj"><div></div></div>
                            <div class="gk"><div></div></div>
                            <div class="tm">2017.10</div>
                            <div class="tm1">2017.11</div>
                            <div class="tm2">2017.11</div>
                            <div class="tm3">2018.01</div>
                            <div class="tm4">2018.02</div>
                            <div class="tm5">2018.04</div>
                            <div class="lc">云设计V1.0设计开始</div>
                            <div class="lc1">云设计V1.0 正式开发</div>
                            <div class="lc2">推荐配置功能上线</div>
                            <div class="lc3">自动化拓扑功能上线</div>
                            <div class="lc4">多云价格优选功能上线</div>
                            <div class="lc5">云设计经典版上线</div>
                       </div>
                    </div>
                  
                </div>
            </div>
      
            <div style="background:#ededed;;width:100%;height:auto;">
                <div class="seleconeMain-footer">
                    <div class="container text-left" style="width:60%;padding-left:cd30px;">
                            <div class="col-md-3 col-xs-12" style="margin-top:27px;margin-bottom:20px;"><img src="../../../assets/qian.png" alt="" style="width:18%;margin-right:10px"><span style="font-size:14px;color:#333333">5天无理由退款</span></div>
                            <div class="col-md-3 col-xs-12 juzhong " style="margin-top:27px;margin-bottom:20px;"><img src="../../../assets/24fuwu.png" alt="" style="width:18%;margin-right:10px"><span style="font-size:14px;color:#333333">7×24小时顾问支持</span></div>
                            <div class="col-md-3 col-xs-12 juzhong " style="margin-top:27px;margin-bottom:20px;"><img src="../../../assets/1fuwu.png" alt="" style="width:18%;margin-right:10px;" class="imgeys"><span style="font-size:14px;color:#333333">1V1专家服务</span></div>
                            <div class="col-md-3 col-xs-12 juright" style="margin-top:27px;margin-bottom:20px;padding-right:40px !important;"><img src="../../../assets/90fuwu.png" alt="" style="width:22%;margin-right:10px"><span style="font-size:14px;color:#333333">90秒极速响应</span></div>
                    </div>
                </div>
            </div>
    </div>
    <Sex></Sex>
</div>


</template>
<style>
.dv2:hover{
    cursor:pointer;
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
.tm,.tm1,.tm2,.tm3,.tm4,.tm5{
    font-size:12px;
    color:#e41e2b;
}
.tm{
     position:absolute;
    top:-45px;
    left:8%;
}
.tm1{
     position:absolute;
    top:-45px;
    left:25%;
}
.tm2{
     position:absolute;
    top:-45px;
    left:39%;
}
.tm3{
     position:absolute;
    top:-45px;
    left:54%;
}
.tm4{
     position:absolute;
    top:-45px;
    left:70%;
}
.tm5{
    position:absolute;
    top:-45px;
    left:89%;
}
.lc,.lc1,.lc2,.lc3,.lc4,.lc5{
    font-size:12px;
    color:#666666;
}
.lc{
       position:absolute;
        top:45px;
        left:4%;
}
.lc1{
       position:absolute;
        top:45px;
        left:20%;
}

.lc2{
       position:absolute;
        top:45px;
        left:36%;
}

.lc3{
       position:absolute;
        top:45px;
        left:50%;
}
.lc4{
       position:absolute;
        top:45px;
        left:66%;
}
.lc5{
       position:absolute;
        top:45px;
        left:85%;
}
.ga{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    top:-10px;
    left:-2px;
}
.gs{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:10%;
    top:-10px;
}
.gd{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:27%;
    top:-10px;
}
.gf{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:41%;
    top:-10px;
}
.gg{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:56%;
    top:-10px;
}
.gm{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:72%;
    top:-10px;
}
.gj{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:90%;
    top:-10px;
}
.gk{
    width:20px;height:20px;
    background:#cccccc;
    box-shadow:0 0 1px 0 rgba(182,182,182,0.50);
    border-radius:100px;
    display: table-cell;vertical-align: middle;
    position:absolute;
    left:100%;
    top:-10px;
}
.ga div{
    background:#ffffff;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gs div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gd div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gf div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gg div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gm div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gj div{
    background:#da121a;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
.gk div{
    background:#fff;
    width:10px;
    height:10px;
    border-radius:100%;
    margin:0 auto;
    line-height:10px;
    margin-top:5px;
}
@media (max-width: 768px){
    .tuopus{
        width:110% !important;
    }
      .juright,.juzhong{
          text-align:left !important;
      }
      .ljs{
            width:100%;
            display:inline-block;
            margin-bottom:10px;
        }
        .imgets{
            display:none;
        }
        .iks{
            margin-left:0px !important;
        }
        .naver .row div{
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
@media (min-width: 768px){
    .tuopus{
        width:63% !important;height:63% !important;
    }
    .juright{
        text-align:right;
    }
    .juzhong{
        text-align:center;
    }
      .ljs{
          width:16%;
          display:inline-block;
      }
      .imgets{
          display:inline-block;
      }
      .ik img{
         width:80px;
      }
      .iks{
        margin-left:20px !important;
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
    .lastus{
        margin-top:138px;
    }
    .seleconeMain-mainfir{
        margin-bottom:50px;
    }
    .imgeys{
        margin-left:20px !important
    }
    .color_999{
        line-height:20px !important;
    }
}
@media (max-width: 768px) {
    .hideens{
        display:none;
    }
    .lastus{
        margin-top:10px;
        margin-bottom:20px;
    }
    .imgeys{
        margin-left:0px !important
    }
    .seleconeMain-mainfir{
        margin-bottom:0px;
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
   .selectHelp{
        background:url("../../../assets/er-icon/bgs.png") no-repeat;text-align:center;background-size:100% 100%;
   }

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
                             //console.log($("#ProductFeatures").offset().top - $(window).scrollTop());
                             if($(window).scrollTop()+70>=$("#ProductFeatures").offset().top){
                                $(".rightBs ul li").css("background","#d8d8d8") 
                                $(".nexton").css("background","#da121a")
                             }
                             if($(window).scrollTop()+70>=$("#CoreStrengths").offset().top){
                                  $(".rightBs ul li").css("background","#d8d8d8") 
                                    $(".nextsec").css("background","#da121a")
                             }
                            if($("#QuickStart").length>0){
                                if($(window).scrollTop()+70>=$("#QuickStart").offset().top){
                                    $(".rightBs ul li").css("background","#d8d8d8") 
                                        $(".nextthe").css("background","#da121a")
                                }
                            }
                             if($("#he").height()-($(window).height()+$(this).scrollTop())<50){
                                 $(".rightBs ul li").css("background","#d8d8d8") 
                                  $(".nextf").css("background","#da121a")  
                             }
                        }
                    });
            
                   


              })
 import Sec from "../../../components/SecondaryPages/SecondaryPages.vue"
 import Sex from "../../../components/SecondaryPages/SecondaryFooter.vue"
 import fixedbox from '../../../components/SecondaryPages/protalFixed.vue';
    export default{
         name: 'clouddesignning',
        components:{
            Sec,
            Sex,
            fixedbox
        },
        data(){
            return{ 
            }
        },
        methods:{
              ctaCloundCsbs:function(){
                    window.open("http://demo.csb-china.com")
                },
            spanTy:function(){
                this.$router.push({path: '/login'});
            },
            lj:function(){
                this.$router.push({path: '/registerOne'});
            },
        },
        mounted:function(){
               $(".rightBs ul li").click(function(e){
                               //$(".rightBs ul li").css("background","#d8d8d8");
                               var s = $(this).index();
                             $(".rightBs ul li").not($(this)).css("background","#d8d8d8")
                             $(this).css("background","#da121a")
                             var target = e.target;
                             var id = $(target).data("to");
                             $('html,body').animate({scrollTop:$('.'+id).offset().top+90}, 800);
                            
                         
                         })
                          $(".scrollUp").click(function(){
                                $('html ,body').animate({scrollTop: 0}, 300);
                                return false;
                            });
                        //   $(".rightBs ul li").click(function(e){
                        //      var target = e.target;
                        //      var id = $(target).data("to");
                        //      $('html,body').animate({scrollTop:$('.'+id).offset().top}, 800);
                        //      $(".rightBs ul li").css("background","#d8d8d8");
                        //      $(this).next().css("background","#da121a")
                        //     //  if($(this).index()==0){
                        //     //      var a = '<a href="#cg"></a>';
                        //     //      $(this).append(a)
                        //     //       $(this).find("a").trigger("click");
                        //     //  }
                        //  })
        }
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
    }
</script>