<template>
    <div class=" obj-friend footer">
        <div class="container">
      <!--<div class="container"> -->
        <div class="row" style="margin:0 auto !important;">
                <div class="col-xs-12 col-sm-3 obj-what-dv footer-ts pag">
                <p class="text-left footer-jx">联系我们</p>
                <p class="text-left footer-list hoverRed hovera"><img src="../../assets/phones.svg" alt="" style="width:9px;height:12px">&nbsp<a style="color:#b3b3b3;width:auto !important" href="tel:4008287308">010-12345678</a></p>
                <p class="text-left footer-list hoverRed hovera"><img src="../../assets/mes.svg" alt="" style="width:9px;height:10px">&nbsp<a style="color:#b3b3b3;width:auto !important;display:inline" href="mailto:Help@csb-china.com" >1234567@company.com</a></p>
                <p class="text-left footer-list hoverRed"><img src="../../assets/dizhiicon.svg" alt="" style="width:9px;height:10px">&nbsp北京市海淀区中关村大街18号</p>
                </div>
                
                <div class="col-xs-12 col-sm-3 obj-what-dv footer-ts pkd">
                <p class=" footer-jx text-left">IT动态</p>
                <p class="text-left footer-list hoverRed"><span @click="yungh">新闻动态</span></p>
                <p class="text-left footer-list hoverRed"><span @click="cloundSelect">行业头条</span></p>
                <p class="text-left footer-list hoverRed"><span @click="cloundCe">社群</span></p>
                <p class="text-left footer-list hoverRed"></p>
                </div>
                <div class="col-xs-12 col-sm-2 obj-what-dv footer-ts pkd">
                <p class=" footer-jx text-left">关于我们</p>
                <p class="text-left footer-list hoverRed"><span @click="yunghs">公司简介</span></p>
                <p class="text-left footer-list hoverRed"><span @click="cloundSelects">招贤纳士</span></p>
                <p class="text-left footer-list hoverRed"></p>
                </div>
                <div class="col-xs-12 col-sm-2 obj-what-dv footer-ts pad">
                <p class="text-left footer-jx">服务与支持</p>
               <!-- <p class="text-left footer-list hoverReds" @click="helpCenter">帮助中心</p>
                <p class="text-left footer-list hoverReds" @click="fuwuLook">服务条款</p>-->
                <p class="text-left footer-list hoverReds" @click="feedbacks">意见反馈</p>
               <!-- <p class="text-left footer-list hoverReds" @click="yijianlook">意见反馈</p> -->
                </div>
                <div class="col-xs-12 col-sm-2 obj-what-dv footer-ts footer-left pagd">
                    <div class="lerf">
                <p class="footer-jx">CloudBroker</p>
                    <div class="footer-ke">
                        <p>您专属的云顾问</p>
                        <img src="../../assets/erweima.jpg" alt="" style="width:60px;height:60px">
                    </div>
                </div>
                </div>
        </div>
            
 
        </div>
        <div>
            <div class="footer-inert"></div>
            <div class="row footer-last" style="margin-bottom:0px !important">       
                <p class="text-center thin col-xs-12" style="text-align:center;margin-left:20px;line-height:20px">
                    版权所有 © 2018 北京卓学动力科技有限公司
                    <a style="color:#b3b3b3;width:180px !important;" href="http://www.miitbeian.gov.cn/" target="_blank">
                        苏ICP备18002559号-2
                    </a>
                    
                </p>
            </div>
        </div>
      </div>
</template>
<style scoped>
/**{
   overflow:hidden
}*/
.hoverRed span:hover{
    color:#e41e2b
}
.hoverReds:hover{
    color:#e41e2b
}
.hovera a:hover{
     color:#e41e2b !important
}
.footer-jx:hover{
   cursor:pointer;
}
.footer-list:hover{
     cursor:pointer;
}
.container{ 
    max-width: 1090px;
}
.row{
    margin-right:66px;
    margin-left:66px;
}
.lis-hov:hover{
    filter:alpha(Opacity=80);-moz-opacity:0.8;opacity: 0.8;
    /*background:#1f2745*/
}

.homepage {
    background: #f8f8f8;
    
}

h3{
  margin-top:0;
}
* {
  font-family: "Microsoft YaHei";
}

.friendContainer{
    width:78%;
    padding:20px 0 20px 0;
}
.
ul,ol li {
  list-style: none
}

#carousel-example-generic{
    height:600px;
}
.lunmain {
    background: url('../../assets/Rectangle 10.png') no-repeat; background-size:100% 100%; width: 100%; height: 600px; 
}
.lumain{
    background: url('../../assets/li.png') no-repeat; background-size:100% 600px;width:100%; height: 600px;position: relative
}
.lumain .posiAbout{

    position:absolute;
    right:8%;
    top:10%;
}
.lumain .posiAbout img{
    width:80%;
    height:80%;
}
.navbar {
    background: #2b2b2b; border: none
}
.carousel-inner{
    margin-bottom:0px !important;
}
.ourPoint{
    background:#f7f7f7; padding-bottom: 30px;
}

@media (min-width: 768px) {

.pag{
    padding-left:20px;
}
.pad{
    padding-left:3%;
}   


.lerf{
    border-left:1px solid #2e383e;
    padding-left:8%;
}
 .footer-inert{
    width:101.2%;
    height:2px;
    background:#2e383e;
    margin-top:20px;
}
  .tuPa {
      left: 2%; height: 288px; position: absolute; bottom: -14%
  }
  .cla {
      margin-left: 8%;
  }
  .cl {
      margin-left: 40%;
  }
  .log {
      margin-right: 20px;
  }
  .lunmain .lun-le {
      padding-top: 180px; padding-left: 48px; text-align: left;
  }
  .lumain .lun-le {
      padding-top: 180px; padding-left: 48px; text-align: left;
  }
  .lunmain .lun-rig {
      padding-top: 150px; padding-left: 50px
  }
   .lumain .lun-rig {
      padding-top: 150px; padding-right: 50px
  }
  .Imgs {
     margin-top: 15px;
  }
  .navbar ul li a:hover {
      border-bottom: 1px solid #fff; cursor: pointer;
  }
  .carousel-inner .item img {
      display: inline-block; vertical-align: baseline;
  }
}
.lunmain .lun-le h1 {
    font-size: 28px; color: #f6f6f6; margin-bottom: 10px;
    
}
.lunmain .lun-le .pCenter {
    color: #f0f0f0; font-size: 14px
}
.lunmain .lun-le .pBottom {
    margin-top: 20px;
}
.lunmain .lun-le .pBottom span {
    padding: 10px 25px; border: 1px solid #ccc; color: #fff; font-size: 12px;
}
.lunmain .lun-le .pBottom .pSpan {
    background: #da121a; border-color: #da121a; cursor:pointer;
}
.lumain .lun-le h1 {
    font-size: 26px; color: #f6f6f6; margin-bottom: 10px;
    font-weight:100;
}
.lumain .lun-le .pCenter {
    color: #f0f0f0;   font-size:28px;
}
.lumain .lun-le .pBottom {
    margin-top: 20px;
 
}
.lumain .lun-le .pBottom span {
    padding: 10px 25px; border: 1px solid #ccc; color: #fff; font-size: 12px;
}
.lumain .lun-le .pBottom .pSpan {
    background: #da121a; border-color: #da121a; cursor:pointer;
}
.Imgs {
    width: 144px; height: 19px;
}
.navbar-right ul li span {
    padding: 5px 15px; cursor: pointer;
}
.navbar li a {
    color: #fff !important;
}
.navbar li a:hover {
    color: #fff; text-decoration: none
}
.log {
    border: 1px solid #ccc; color: #e5e5e5;
}
.resc {
    background: #da121a; border: 1px solid #da121a;
}
.navbar-brand {
    padding: 10px 15px;
}

.left,.right {
    width: 5%;
    height:100%;
    background:none !important;
}
.navbar-nav li a:hover {
    border-bottom: 1px solid #fff
}
.imgs {
    width: 100px; height: 60px; margin-left: 150px;
}
.headroom {
    -webkit-transition: all 0.4s ease-out; -moz-transition: all 0.4s ease-out; -o-transition: all 0.4s ease-out; transition: all 0.4s ease-out;
}
.jz-img{
     -webkit-transition: all 0.6s ease-out; -moz-transition: all 0.6s ease-out; -o-transition: all 0.6s ease-out; transition: all 0.6s ease-out;
}
.navbar-inverse {
    height: 80px; border: none
}
.navbar-nav li span {
    color: #fff;
}

.annou {
    font-size: 18px; color: #da121a; text-align: left
}
.obj-main {
    width: 100%; background: #fff;
}
.obj-main h1 {
    color: #333333; font-weight: 200; font-size:32px; text-align:center; padding-top:20px;
}
.obj-main h3 {
    font-size:16px; color:#777777; text-align:center;
}
.obj-main .Yunimg {
    /*width: 120px; height: 75px;*/
}
.obj-main .obj-cta {
    width:120px; height:35px; line-height:35px; background: #da121a; border: 1px solid #da121a; margin-top: 15px; display: inline-block; color: #ffffff; cursor:pointer;
  font-size: 14px;
}
.obj-main p {
    font-size: 14px; color: #666666;
}
.obj-main h2 {
    font-size: 20px; color: #333333;
}
.obj-main h4 {
    font-size: 18px; color: #333333;
}
.obj-main .blurb-cta {
    margin-bottom: 30px;
}
.obj-what-dv img {
    width: 100%; height: 100%;
}
.obj-what {
    width: 100%;
}
.obj-what .container {}
.obj-what .container .jzWe {
    margin-bottom: 50px;
}
.obj-what-ds {
    margin-top: 15px;
}
.obj-what-ds h1 {
    font-size: 44px;
}
.obj-what-ds h1 img {
    width: 45px; height: 49px
}
.obj-what-ds h3 {
    font-size: 28px; color: #666666;
}
.obj-what-ds p span {
    font-size: 12px; color: #ffffff; background: #0983f6; border-radius: 4px; border: 1px solid #0983f6; margin-right: 5px;
}
.obj-what-ds p {
    margin-top: 30px;
}
.obj-what-ds p span:nth-child(1) {
    padding: 5px 15px;
}
.obj-what-ds p span:nth-child(2) {
    padding: 5px 25px;
}
.obj-what-ds p span:nth-child(3) {
    padding: 5px 15px;
}
.obj-what-dc {
    margin-top: 40px;
}
.obj-what-da {
    margin-top: 15px;
}
.obj-chat {
    margin-top: 50px;
}

.obj-friend {
    background: #f8f8f8; width: 100%; padding-bottom: 50px; margin: 0;
}
.obj-chat,.obj-what h1 {
    color: #333333;
}
.jsFei {
    margin-top: 50px;
}
.jzfei img {
    padding-bottom: 20px;
}
.obj-free {
    width: 100%; background: #da121a; background-size: cover; height: auto;
}
.obj-free p {
    font-size: 14px; color: #ffffff; line-height: 44px; font-weight: 200; padding-top: 30px; padding-bottom: 30px;
}
.obj-free span {
    border: 1px solid #fff; font-size: 14px; color: #ffffff; padding: 8px 40px;
}
.obj-free .container {
    width: 80%;
}
.footer {
    background: #2b2b2b; min-height:170px;
}
.footer .footer-ts {
    margin-top: 20px;
}
.footer p {
    font-size: 12px; color: #b3b3b3; line-height:17px;
}
.footer-ts img {
    width: 59px; height: 59px;
}
.footer .container {
    width: 60%;
}


.footer .footer-jx {
    font-weight: 200; font-size:14px; color:#ccc;
}
.footer-list{
    font-size:12px; color:#b3b3b3;
}
.footer .footer-last {
    margin-top: 20px; line-height: 62px;background:#2b2b2b;
}
.footer .footer-last p {
    font-size: 12px; color: #b3b3b3; text-indent:-50px; line-height:10px;
}
.footer .footer-last p:nth-child(1){
    margin-top:15px;
}
.footer {
    padding-bottom: 0;
}
.dis {
    padding: 50px;
}
.lun-rig img {
    /*width: 426px; height: 303px;*/
}
@media (max-width: 768px) {
    .footer .footer-left {
       
    }
    .lerf{
         border-left:0px solid #2e383e;
    }
.footer-inert{
    width:0;
    height:0px;
    background:#2e383e;
    margin-top:0px;
}
.right{
    height:100%;
}
.lunmain .container {
  width: 100%; margin-top: 10%;
}
.tuPa {
  right: 0; height:0%; position: absolute; bottom: 0
}
.lun-rig img {
  width: 100%; height: 100%; margin-top: 50px;
}
.dsg {
  padding: 0
}
.obj-chat {
  margin-top: 0;
}
.obj-what {
  margin-bottom: 0px;
}
.obj-main .blurb-cta {
  margin-bottom: 50px;
}
.obj-what-da {
  margin-bottom: 30px;
}

.annou {
  text-align: center;
}
#bs-example-navbar-collapse-1 {
  background: #000;
}
.obj-what-ds p span:nth-child(1) {
  padding: 5px 0px;
}
.obj-what-ds p span:nth-child(2) {
  padding: 5px 10px;
}
.obj-what-ds p span:nth-child(3) {
  padding: 5px 0px;
}
}
.phone-position {
  position: relative
}

.router-link-d {
    color: #000;
}
a:hover {
    text-decoration: none
}
.logoutbtn {
    padding: 5px 20px !important; border:none; color:#fff;
}
.realname-san{
    width: 0;
    height: 0;
    margin-left: 8px;
    display:inline-block;
    vertical-align: middle;
    border-top: 4px dashed;
    border-top: 4px solid;
    border-right: 4px solid transparent;
    border-left: 4px solid transparent;
}
.logout-box{
    position:relative;
}
.logout-ul{
    position:absolute;
    width:80px;
   
    right:0;
    top:50px;
    background:#fff;
}
.logout-ul li {
    width:100%;text-align: center; line-height: 20px;
}
/*.bluar-ccc {
    border: 1px solid #f7f7f7; background: #f7f7f7; color: #999; border-radius: 2px; font-size: 14px; padding: 10px; height:140px; line-height:1.5; margin-top:20px;
}*/
h2 {
    font-size: 20px;
}
.obj-what container {
    background: #f7f7f7;
}
.obj-what-whew{
    padding:20px 0 20px 0;
}
.obj-what-whew h2 {
    font-size: 32px; font-weight:200; color: #333333;
}
.p-wha {
    font-size: 16px; color: #777777;
}
.heng {
    background: #da121a; margin: 0 auto; width: 60px; height: 3px; margin-bottom: 30px;
}
.pS {
    color:#666;
}
.color_999{
    color:#999;
}
.mainPd {
    margin-top: 20px; color: #666666; display: block
}
.mainpa {
    font-size: 14px; color: #666666; line-height: 12px;
}
.mainpa p {
    color: #666666; display: block
}
.obj-lhat {
    background: #fff;
}
.obj-lhat .lhat-td {
    margin-top: 35px;
}
.obj-lhat .expru {
    padding-bottom: 40px;
   
}
.he-su {
    background: #da121a; margin: 0 auto; width: 60px; height: 3px; margin-bottom: 30px;
}
/*@-webkit-keyframes rotation {
  from {
    -webkit-transform: rotate(0deg);
  }
  to {
    -webkit-transform: rotate(360deg);
  }
}
.tranImg:hover{
   
   -moz-animation:rotation 2s linear infinite; 
    -webkit-animation:rotation 2s linear infinite;
    -o-animation:rotation 2s linear infinite
}*/
.ths {
    font-size: 36px;
}
.li-fir {
    background: url('../../assets/Group 28.png') no-repeat; text-align: center; margin: 0 auto; width: 273px; height: 376px;
}
.li-sec {
    background: url('../../assets/Group 24.png') no-repeat; text-align: center; margin: 0 auto; width: 273px; height: 376px;
}
.li-the {
    background: url('../../assets/Group 22.png') no-repeat; text-align: center; margin: 0 auto; width: 273px; height: 376px;
}
.pict {
    width: 54px; height: 60px; transition: all 0.6s;   margin-top: 30%;
}
.picts {
    width: 70px; height: 60px; transition: all 0.6s;  margin-top: 30%; margin-left: 4%;
}
.pictes .dnsery{
    position:absolute;
    left:0;
    top:0;
    width:273px;
    height:376px;
     filter:alpha(Opacity=80);-moz-opacity:0.8;opacity: 0.8;
    background:#1f2745
}
.li-fir,.li-sec,.li-the p {
    font-size: 14px; color: #e5e5e5; text-align: center;
}
.li-fir h2{
    font-size:20px; color:#ffffff; text-align:center; font-size:20px;
}
.li-sec h2{
    font-size:20px; color:#ffffff; text-align:center; font-size:20px; padding-left:2%;
}
.li-the h2{
    font-size:20px; color:#ffffff; text-align:center; font-size:20px;
}



.obj-frees{
    width: 100%; background: #e41e2b; background-size: cover; height: auto;
}
.obj-frees p {
    font-size:24px; color:#ffffff;  text-align:center;font-weight:200;
}
.obj-frees span {
    border: 1px solid #fff; display:inline-block; font-size: 14px; margin-top:10px; color: #ffffff; cursor:pointer;  transition: all .25s ease; padding: 4px 20px;
}
.obj-frees span:hover{
    background:#fff; color:#da121a;
}
.jsFei h1{
    font-size:32px; color:#333333; font-weight:200; text-align:center;
}
.jsFei h3{
    font-size:16px; color:#777777; text-align:center;
}
  .pder{
      position:absolute; top:0%;left:0%;
      width:100%;
  }
  .pder h4{
          font-size: 32px;
         margin: 50px 0 25px;
         color:#fff;
  }

.tranimg:hover{
      transform: scale(1.2);
        -webkit-transition: all 0.6s ease-out; -moz-transition: all 0.6s ease-out; -o-transition: all 0.6s ease-out; transition: all 0.6s ease-out;

}
.PlanLj{cursor:pointer;-webkit-animation: scaleout 1s infinite ease-in-out;animation: scaleout 1.5s infinite ease-in-out;}
@-webkit-keyframes scaleout{
    0% { -webkit-transform: scale(1.0) }
    10%{-webkit-transform: scale(1.05);
        opacity: 0.9;
    }
    25%{
        -webkit-transform: scale(1.1);
        opacity: 0.8;
    } 
    40%{-webkit-transform: scale(1.15);
        opacity: 0.7;
    }
    50%{
        -webkit-transform: scale(1.2);
        opacity: 0.6;
    }
    65%{
        -webkit-transform: scale(1.15);
        opacity: 0.7;
    }
    75%{
        -webkit-transform: scale(1.1);
        opacity: 0.8;
    }
    90%{
        -webkit-transform: scale(1.05);
        opacity: 0.9;
    }
    100% {
        -webkit-transform: scale(1.0);
        opacity: 1;
    }
      
}
@keyframes scaleout {
    0% { -webkit-transform: scale(1.0) }
    10%{-webkit-transform: scale(1.05);
        opacity: 0.9;
    }
    25%{
        -webkit-transform: scale(1.1);
        opacity: 0.8;
    } 
    40%{-webkit-transform: scale(1.15);
        opacity: 0.7;
    }
    50%{
        -webkit-transform: scale(1.2);
        opacity: 0.6;
    }
    65%{
        -webkit-transform: scale(1.15);
        opacity: 0.7;
    }
    75%{
        -webkit-transform: scale(1.1);
        opacity: 0.8;
    }
    90%{
        -webkit-transform: scale(1.05);
        opacity: 0.9;
    }
    100% {
        -webkit-transform: scale(1.0);
        opacity: 1;
    }opacity: 0.5;
      
}
.blurb-cta{
    padding-top:20px
}
.blurb-cta span{
    margin-bottom:20px;
}
.claes{
    padding:20px 0 20px 0 ;
}
 .imgAnimation{  
      animation-name: imgAnimation;  
      animation: imgAnimation 2s infinite  linear  ;
      -webkit-animation: imgAnimation 2s infinite  linear ;  
      -moz-animation: imgAnimation 2s infinite  linear ;  
 }  
 @-webkit-keyframes imgAnimation{  
    from{ -webkit-transform: rotate(0deg)}  
    to{ -webkit-transform: rotate(360deg)  
   }  
 }  

</style>
<script>
    export default{
        methods:{
            cloundCes:function(){
                this.$router.push({path: '/openCourse'});
                    $('html ,body').animate({scrollTop: 0},0);
            },
            cloundSelects:function(){
                  this.$router.push({path: '/classProcess'});
                    $('html ,body').animate({scrollTop: 0},0);
            },
            yunghs:function(){
                 this.$router.push({path: '/bigcafeTeam'});
                    $('html ,body').animate({scrollTop: 0},0);
            },
            cloundPlan:function(){
                  this.$router.push({path: '/cloudplanning'});
                    $('html ,body').animate({scrollTop: 0},0);
            },
            cloundSelect:function(){
                  this.$router.push({path: '/industryheadlines'});
                    $('html ,body').animate({scrollTop: 0},0);
            },
            cloundCe:function(){
                  this.$router.push({path: '/zxdlcommunity'});
                    $('html ,body').animate({scrollTop: 0},0);
            },
            fuwuLook:function(){
                  this.$router.push({path: '/newsdynamic'});
                   $('html ,body').animate({scrollTop: 0},0);
            },
            yungh:function(){
                    this.$router.push({path: '/newsdynamic'});
                   $('html ,body').animate({scrollTop: 0},0); 
            },
            yungm:function(){
                    this.$router.push({path: '/cloudbuying'});
                   $('html ,body').animate({scrollTop: 0},0); 
            },
            yunsj:function(){
                    this.$router.push({path: '/clouddesignning'});
                   $('html ,body').animate({scrollTop: 0},0); 
            },
            cloundsj:function(){
                    this.$router.push({path: '/wudata'});
                   $('html ,body').animate({scrollTop: 0},0); 
            },
            yijianlook:function(){
                   this.$router.push({path: '/wudata'});
                   $('html ,body').animate({scrollTop: 0},0); 
            },
            helpCenter:function(){
                //   var that = this; 
                  var win = window.open("http://xiaowei.io/chat/pc/index.html?appid=3311&style=red","_blank","height=600,width=500","top=0,left=0,toolbar=yes,menubar=yes,scrollbars=no,resizable=no,location=no,status=no");
//var win = window.open("#/CustomerService","_blank","height=600,width=500","toolbar=yes, location=no, directories=no, status=no, menubar=no, scrollbars=yes, resizable=no, copyhistory=yes");
            },
            feedbacks:function(){
                this.$router.push({path: "/selfeedback"})
                 $('html ,body').animate({scrollTop: 0},0); 
            }
        },
        mounted:function(){
            if(document.documentElement.clientWidth>=1024){
                    $(".liHoversBj a").removeAttr('href');
               
            }else if(document.documentElement.clientWidth<1024){
                    $(".liHoversBj a").attr('href',"tel:4008287308");
            }
        }
    }
</script>
