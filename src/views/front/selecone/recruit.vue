<template>
  <div>
    <!-- 悬浮框 -->
    <!--<fixedbox></fixedbox>-->
    <div style="background:#f5f5f5;width:100%;height:70px;line-height:70px;" class="displayshow">
      <div class=" fixshow fis container">
        <div class="col-md-2 col-xs-2"><a href="#ProductFeatures"><i class="iconfont icon-tuandui"></i> 关于我们</a></div>
        <div class="col-md-2 col-xs-2"><a href="#CoreStrengths"><i class="iconfont icon-shenpiliucheng"></i> 我们的发展</a></div>
        <div class="col-md-2 col-xs-2"><a href="#QuickStart"><i class="iconfont icon-jibenxinxi"></i> 企业文化</a></div>
        <div class="col-md-2 col-xs-2"><a href="#qualification"><i class="iconfont icon-shu"></i> 我们的资质</a></div>
        <div class="col-md-2 col-xs-2"><a href="#ContactUs"><i class="iconfont icon-kefu"></i> 联系我们</a></div>
      </div>
    </div>
    <Sec active="9"></Sec>
    <div class="cloundcompare">
      <div class="cloundbanner">
        <div class="container">
          <div class="clound-dvs col-xs-12">
            <!--<p class="clound-ps">我们每前进一小步，都将竭力为您带来更好的云中服务！</p>-->
            <p class="clound-ps">我们每前进一小步，都将竭力为您带来新兴技术推广服务！</p>
            <!--  <p class="clound-pa">让每一个上云者都在我们（CSB ²）的帮助下，找到并用好适合自己的云</p>-->
            <p class="clound-pa">让每一个初学者都在我们（ZXDL）的帮助下，找到并深入学习适合自己的IT技能</p>
            <p class="clound-pd">我们目标是成为促进新兴技术普及和推广的服务者</p>
            <!-- <p class="clound-pg" style="margin-bottom:110px;"><span @click="ctaCloundCsbs"></span></p>--><br/><br/><br/><br/><br/><br/><br/>
          </div>
        </div>
      </div>
      <div id="recruit" v-show="isShow">
        <div class="nav-bottom-kk"></div>
        <div class="container">
          <div class="cloundMains-main">
            <div class=" text-left redtitle">
              <span class="redLine"></span><span class="redlasttitle">招贤纳士</span>
            </div>
            <div class="" class="text-left drea">
              <!--<div class="dibvs">
                  <span class="">地区：</span>
                  <select class="slesa" v-model="region" @change="getAllRecruit" >
                    <option value="">请选择</option>
                    <option :value="item.id" v-for="item in regions">{{item.name}}</option>
                  </select>
              </div>-->
              <!-- <div class="dibvs">
                  <span class="gws">岗位：</span>
                  <select class="slesa" v-model="job"   @change="getAllJobs"  >
                    <option value="">请选择</option>
                    <option :value="item.recruit_type" v-for="item in jobs">{{item.recruit_type}}</option>
                  </select>
              </div> -->
              <!-- <button class="tems teamdia-btn-save" v-on:click="getprof()">查询</button> -->

              <div class="clear"></div>

            </div>
            <hr/>
            <div>
              <div class="">
                <div>
                    <div class="text-left zptitle">
                      <span>行政专员</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：1名</span></span><br/>
                    </div>
                    <div>
                      <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.负责公司固定资产、办公用品的管理工作；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.负责公司环境卫生管理、办公设备等综合事务工作；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.负责公司相关证件、文件、合同、公章等资料保管及借阅管理工作；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.为公司所有部门提供必要的办公设施及其他后勤支持；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.完成上级安排的其他事宜。</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.女，大专以上学历；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.身高165cm以上，性格开朗活泼开朗；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.有一年以上相关工作经验，具备一定的行政管理知识；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.具备良好的沟通协调能力，工作积极主动，执行力较强；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.熟练使用日常办公软件，熟悉固定资产、档案文书的管理；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.有一定的抗压能力及团队合作精神。</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;备注：简历中请附带一张本人近期照片</div>
                    </div>
                    <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                    <div class="text-left zptitle">
                      <span>外呼线上咨询顾问</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：5名</span></span><br/>
                    </div>
                    <div>
                      <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.通过电话访问，了解客户需求，给意向客户提供专业的介绍</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.准确录入客户基本信息及问题，预约信息、回访信息，提高客户的满意度与认知度；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.按照客户的需求将客户安排进一步沟通工作；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.不断提升外呼水平，及时总结，协助上级完成外呼目标和任务。</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.女，大专以上学历，有客服、外呼工作经验者优先；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.普通话标准，无口音，讲话有条理，亲和力强，吐字清晰流畅，具有良好的沟通能力；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.服务意识强，能承受工作压力；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.工作热情，积极主动，有责任感及良好的团队合作意识和自我管理能力；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.熟练使用办公软件，善于利用及时通信方式沟通交流；</div>
                      <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.具备一定的销售推广经验，良好的服务意识者优先考虑。</div>
                    </div>
                    <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                  <div class="text-left zptitle">
                    <span>客服咨询顾问</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：2名</span></span><br/>
                  </div>
                  <div>
                    <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.负责及时回复客户在线上/线下提出的相关咨询问题，帮助客户解决疑问；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.以客户保持良好的互动与沟通，提升客户的满意度，做好用户关系维护；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.根据客户的反馈和建议，整理后提交给相关业务主管，帮助改进和提升；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.积极办理好领导布置的其他工作任务。</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.女，大专以上学历，熟练掌握电脑，熟练使用各类办公软件；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.有较强的客服意识、耐心和责任心，工作积极主动；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.有较强的沟通能力，文字语言表达流利，学习能力强；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.具备良好的心理素质，能进行自我调节，抗压强，能吃苦；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.有良好的应变能力、协调能力，能处理紧急问题。</div>
                  </div>
                  <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                  <div class="text-left zptitle">
                    <span>微信运营</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：1名</span></span><br/>
                  </div>
                  <div>
                    <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.负责企业微信公共号的运营、更新及维护，增加粉丝数、提高活跃度，提升品牌影响力和关注度；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.利用微信平台推广公司的品牌、产品和活动；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.对微信二次开发有一定的了解；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.与平台管理和粉丝建立良好的关系，挖掘和分析用户使用微信习惯、情感及体验感受，及时抓住热点事件进行营销策划；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.了解各类微信活动的策划和实施，跟踪微信推广效果，分析数据并反馈；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.协助领导完成其他基于微信相关的工作安排。</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.有微博微信运营等经验者优先；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.思维活跃，具有一定的能力、表达能力、分析能力、动手能力以及组织协调能力；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.扎实的书面文字语言组织能力、文案撰写能力，具有较好的内容编辑、较强的选题、策划、编辑撰写能力；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.具有较敏锐的市场触觉，关注社会热点，借力宣传公司微信，提供影响力和粉丝量；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.工作效率高，勤奋，扎实，上进，爱学习；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.对自己有明确的职业规划，要求严格，有创业者精神者优先考虑。</div>
                  </div>
                  <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                  <div class="text-left zptitle">
                    <span>Java开发工程师</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：1名</span></span><br/>
                  </div>
                  <div>
                    <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.负责所属模块的功能规划、需求分析设计、技术实现和用户体验；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.负责所属模块的代码开发、调试与维护工作；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.积极响应客户需求并进行开发和交付；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.参与公司产品的架构优化，性能优化并辅助其他模块进行技术实现；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.协助并完成其他各类技术开发任务。</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.计算机或者相近专业，统招全日制本科以上学历；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.良好的问题理解能力，能够理解以及处理复杂逻辑；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.具备较强的自学能力，团队精神及抗压能力；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.1-2年以上的Java开发经验，掌握JSDK,J2EE的相关知识，熟悉Java、jsp、serverlet编程；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.熟悉多线程，熟练掌握Ajax，jquery；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.熟练掌握Java script脚本编写，了解xml，xslt，css的相关知识；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7.掌握数据库的相关知识，熟悉sqlserver及oracle，具备sql、触发器、函数、存储过程的编写能力；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;8.具备一定的文档编写能力，了解UML。</div>
                  </div>
                  <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                  <div class="text-left zptitle">
                    <span>web前端开发工程师</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：1名</span></span><br/>
                  </div>
                  <div>
                    <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.前端底层框架搭建，基础组建的搭建与维护，为团队其他成员提供调用能力；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.负责官网前后台、微信网站等前端页面开发制作，以及前端与业务层交互设计、开发和维护；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.持续的优化前端体验和页面响应速度，优化代码并保持良好兼容性，提升易用性；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.根据产品需求，分析并给出最优的页面前端结构解决方案；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.善于分享，各种前端疑难问题攻坚，维护并带动团队技术交流和分享活动，促进前端团队共同进步。</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.大专以上学历，计算机相关专业，2-3年以上开发经验；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.良好的学习能力和团队合作精神，逻辑思维强，能够将需求抽象成功能；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.Node.JS使用经验1年以上，熟悉grnut、requirejs、百度FIS等工具；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.精通HTML5及CSS3，熟悉VUE前端框架优先；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.熟练应用多种技巧优化前端页面，有前后端分离方案经验者优先；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6.熟练掌握CMD或AMD规范并有成熟实践者优先；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7.熟悉移动端浏览器渲染原理者优先</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;8.熟悉HTTP协议者，有后端能力者优先。</div>
                  </div>
                  <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                  <div class="text-left zptitle">
                    <span>UI设计师</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：1名</span></span><br/>
                  </div>
                  <div>
                    <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.根据公司产品的定位和需求，负责并设定整体视觉风格和UI设计规范；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.对现有官网及商场页面进行优化，使用户造作更趋于人性化；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.参与团队沟通提出符合产品的设计与体验的解决方案；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.产品广告的设计，公司对外宣传活动的设计；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.完成上级领导交代的临时事项。</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.大专以上学历，1年以上相关工作经验；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.熟悉各类网络平台架构设计；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.善于沟通与协调，良好的团队合作意识。</div>
                  </div>
                  <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
                <div>
                  <div class="text-left zptitle">
                    <span>储备干部（管培生）</span><span class="isol"><span>发布日期：2018/12/19 </span><span class="komns">招聘城市：北京</span><span class="komns"> 招聘人数：3名</span></span><br/>
                  </div>
                  <div>
                    <!--<div v-for="li in item.content" v-if="listyus[index].q==true" class="recruitli">{{li}}</div>-->
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;岗位职责：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.就业发展方向为技术岗位、管理岗位以及项目运营推广方面；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.对各平台数据整理，数据分析，客户数据挖掘，社群维护，提高活跃度。</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任职要求：</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.大专及以上学历；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.具备良好的沟通能力和灵活应变能力；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.愿意从基层做起，认同公司的发展理念和价值观；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.熟练掌握电脑办公软件操作；</div>
                    <div class="recruitli">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.服从公司岗位发展安排。</div>
                  </div>
                  <!-- <textarea class="tytyt" disabled="disabled">{{item.content}}</textarea> -->
                </div>
            <!--    <el-pagination class="adviser-page-bg mianss"  background layout="prev, pager, next" :page-size="10" :total="Number(total)" @current-change="handleCurrentChange">
                </el-pagination>-->
              </div>
            <!--  <div class="design-nodata" v-if="recruitList.length<1">
                <img src="../../../assets/compare-nodata.png" alt="">
                <br>
                暂无招聘信息
              </div>-->

            </div>
          </div>
        </div>
      </div>
      <Sex></Sex>
    </div>
  </div>


</template>
<style>
.recruitli{
  text-align:left;
  line-height:40px !important;
}
.komns{
  margin-left:20px;
}
.tytyt{
  padding-top:10px;
  width:100%;
  height:450px;
  border:none;
  resize:none;
  background:#fff !important;
  padding-left:30px;
  overflow-y:hidden;
}
.mianss{
  margin-bottom:30px;
  margin-top:30px
}
  .zptitle{
    padding:20px 70px;
    margin:20px 0;
    background:#F7F8F9;
    color:#000;
  }
  .isol{
    color:#000;
    float:right;
    margin-right:10%;
  }
  .tems{
    margin-left:10px;
  }
  .navers a i{
    font-size:14px;
    color:#A5A5A5;
  }
   .slesa{
      width:150px;
      height:30px;
      border:1px solid #ccc;
    }
  .navers a:hover{
    cursor:pointer;
    color:#da121a;
    display:inline-block;
    border-bottom:1px solid #da121a;
  }

  .navers i{
    color:#c2c2c2;
  }
  .fixshow i{
    color:#c2c2c2;
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

  .displayshow{
    display:none;
    position:fixed;
    top:0;
    z-index:999999999;
  }
  .dv2:hover{
    cursor:pointer;
  }
  .nav-bottom-kk{
    width:100%;
    height:1px;
    background:#d6d6d6
  }
  .navers{
    height:70px;
    line-height:70px;
  }
  .navers a{
    font-size:14px;
    color:#333333;
  }
  .navers a i{
    font-size:14px;
    color:#A5A5A5;
  }
  .navers a:hover{
    cursor:pointer;
    color:#da121a;
    display:inline-block;
    border-bottom:1px solid #da121a;
  }
  /**/
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
  .Weml{
    font-size:16px;
    color:#333333;
    margin-top:40px;
  }
  .Weml i{
    color:#da121a;
  }
  .Wemls{
    font-size:16px;
    color:#333333;
    margin-top:50px;

  }
  .Wemls i{
    color:#da121a;
  }
  .dsh{
    font-size:14px;
    color:#333333;
    text-indent:1em;
  }
  .dhz{
    margin-bottom:10px;
    margin-top:20px;
  }
  .wey{
    margin-top:20px;

  }
  .defaimg{
    width:550px;
    height:400px;
  }
  .liHoversBj:hover{
    background:#EF131D;
  }
  @media (min-width: 768px) {
    .gws{
      margin-left:30px;
    }
    .dibvs{
      display:inline-block;
    }
    .drea{
      padding-left:70px;
    }

    .juright{
      text-align:right;
    }
    .spanshover{
      display:inline-block;
      padding: 0 10px;
      font-size:14px;
      color:#333333;
    }
    .juzhong{
      text-align:center;
    }
    .navers div{
      margin-right:30px;
    }
    .fis div{
      margin-right:30px;
    }
    .ulsMains{
      margin-left:82px;
    }
    .color_999{
      line-height:20px !important;
    }
    .imgeys{
      margin-left:20px !important;
    }
    .zizhi{
      margin-bottom:70px;
    }
    .cccspan{
      width:316px;
      display:inline-block;
    }
    .yellowSpan{
      width:85px;
    }
    .yellowSpam{
      width:85px;
    }
    .divimger{
      display:block;
    }
    .callmain img{
      height:auto;
      width:100%;
    }
    .werxins{
      /*padding:106px 0px 0px 110px;*/
      font-size:16px;color:#666666;text-align:left;
      padding-left:20px;
    }
  }
  @media (max-width: 768px) {
    .dibvs{
      display:block
    }
    .juright,.juzhong{
      text-align:left !important;
    }
    .navers  div{
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
    }
    .fixshow  div{
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
    }
    .zizhi{
      margin-bottom:40px
    }
    .ulsMains{
      margin-left:0px;
    }
    .imgeys{
      margin-left:0 !important;
    }
    .divSc{
      margin-top:20px !important;
      margin-bottom:20px !important;
    }
    .clound-dvs{
      margin-top:0;
    }
    .cccspan{
      width:150px;
      display:inline;
    }
    .yellowSpan{
      width:78px;
    }
    .yellowSpam{
      width:78px;
    }
    .divimger{
      display:none;
    }
    .callmain img{
      height:auto;
      width:100%;
    }
    .werxins{
      /*padding:106px 0px 0px 0px;*/
      padding-left:0px;
      font-size:16px;color:#666666;text-align:center;
    }

  }

  .callme-call{
    font-size:26px;
    color:#333333;
    margin-bottom:40px;
    font-weight:100;
  }
  .callme-dist .mospan{
    padding:10px 40px;
    display:inline-block;
    background:#f7f7f7;
    border-radius:4px;
    font-size:14px;
    color:#333333;
    margin-right:20px;
    margin-left:20px;
  }
  .moren{
    padding:10px 40px;
    display:inline-block;

    border-radius:4px;
    font-size:14px;

    margin-right:20px;
    margin-left:20px;
    background:#da121a;
    color:#fff;

  }
  .callme-dist span:hover{
    cursor:pointer;
  }
  .yellowSpan{

    display:inline-block;
    height:41px;
    font-size:14px;
    color:#ffffff;
    line-height:40px;
    background:url('../../../assets/yellowright.png') no-repeat;background-size:cover;
  }
  .yellowSpam{
    display:inline-block;

    height:41px;
    line-height:40px;
    font-size:14px;
    color:#ffffff;
    background:url('../../../assets/yellowleft.png') no-repeat;background-size:cover;
  }
  .ulsMains{


  }
  .cccspan{
    background:#f3f4f5;


    height:40px;
    font-size:14px;
    color:#666666;
    line-height:40px;
  }
  .cccspans{
    margin-top:60px;

  }
  .cloundMains-go .wer{
    margin-top:20px;
    font-size: 26px;
    color: #333333;
    text-align: center;
    font-weight:100;
  }
  .cloundMains-main{
    margin-top:30px;
  }
  .cloundMains-main p{
    font-size: 26px;
    color: #333333;
    text-align: center;
    font-weight:100;
  }
  .cloundMains-main div{
    font-size:14px;
    line-height:25px;
  }
  *{
    margin:0;padding:0;
  }
  .container{
    max-width: 1090px;
  }
  .cloundbanner{
    background:url('../../../assets//banner-14.png') no-repeat;background-size:cover;
  }
  .clound-dvs{
    margin-top:112px;
  }
  .clound-ps{
    font-weight: 100;
    font-size: 26px;
    color: rgb(248, 248, 248);
    margin-top:20px;
  }
  .clound-pg span:hover{
    cursor:pointer;
    background:#fff;
    color:#e41e2b;
    border:1px solid #fff;
  }
  .clound-pa{
    font-weight: 100;
    font-size: 16px !important;
    color: rgb(248, 248, 248);
  }
  .clound-pd{
    font-weight: 100;
    color: rgb(248, 248, 248);
    font-size: 16px !important;
  }
  .clound-pg{
    margin-top:30px;
  }
  .clound-pg span{
    border: 1px solid #e41e2b;
    font-size: 12px;
    color: #fff;
    padding: 10px 25px;
    display: inline-block;

    text-align: center;
    background: #e41e2b;
  }
  .city{
    background:url("../../../assets/compares.png") no-repeat  center center;background-size:75%;
  }
  .scrollUp:hover{
    cursor:pointer;
  }
   @media screen and (min-width: 768px) and (max-width:991px ){
            .iks{
                margin-left: 0 !important
            }
            .imgets{
                display: none !important
            }

    }
</style>

<script>
  $(document).ready(function(){
    // $(".rightBs ul li").find("a").click(function(){
    //     // $(".rightBs ul li").css("background","#d8d8d8");
    //     // $(this).css("background","#da121a");
    //     alert(1)
    // });

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

      if($(".navers").length==1){

        var topa = $(".navers").offset().top - $(window).scrollTop();
        if(topa<0){
          $(".displayshow").css("display","block")
        }else if(topa>0){
          $(".displayshow").css("display","none")
          $(".rightBs ul li").css("background","#d8d8d8")
        }

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
          $(".rightBs ul li").css("background","#d8d8d8");
          $(".nextf").css("background","#da121a")
        }
      }
    });
  })
  import '../selecone/bais.css'
  import Sex from "../../../components/SecondaryPages/SecondaryFooter.vue"
  import Sec from "../../../components/SecondaryPages/SecondaryPages.vue"
  import fixedbox from '../../../components/SecondaryPages/protalFixed.vue';
  export default{
    components:{
      Sec,
      Sex,
      fixedbox
    },
    data(){
      return {
        Ais:false,
        Sis:true,
        Asd:false,
        phoneBox:false,
        isShow:true,
        regions:[],
        region:'',
        job:'',
        jobs:[],
        total:'',
        bRecruitBo:{
          pageReq: {
            page: 0,
            size: 10,
          },
          recruitType:null,
          recruitCity:null
        },
        recruitList:[],
        listyus:[],
        ti:[]
      }
    },
   /* methods:{
    /!*  beijingHover:function(){
        this.Asd=true;
        this.Ais=false;
        this.Sis=false;
        $("#bjs").addClass("moren");
        $("#bjs").removeClass("mospan");
        $("#hzs").removeClass("moren");
        $("#hzs").addClass("mospan");
        $("#wxs").removeClass("moren");
        $("#wxs").addClass("mospan");


      },*!/
/!*
      handleCurrentChange:function(val){
        this.bRecruitBo.pageReq.page = val-1;
        this.getprof();
      },
      changety:function(e){
         if( this.listyus[e].q == false ){
            this.listyus[e].q = true
         }else{
            this.listyus[e].q = false
         }
      },*!/
     /!* getprof:function(){
        if(this.isShow==true){
            this.bRecruitBo.recruitCity = this.region;
            this.bRecruitBo.recruitType = this.job;
            this.$this.post('broker/recruit/getAll',this.bRecruitBo).then((response)=> {
              this.recruitList = response.data.content;
              let aaa = '职责要求:↵1.	计算机类相关本科毕业或同等学力，3年或3年以上Java开发经验.↵2.	能对分布式常用技术进行合理应用，解决问题；↵3.	熟练Spring 体系：Spring MVC，Spring data，Spring Boot，Spr';
              for(var i = 0;i<this.recruitList.length;i++){
                  this.listyus.push({q:false})
                  this.recruitList[i].content = this.recruitList[i].content.split('\n');
                  // console.log(this.recruitList[i].content.replace(/[\r\n]/g, ""))
                  // this.ti.push(this.recruitList[i].content.replace(/[\r\n]/g, ""))
              }
              //console.log('----',this.recruitList[0].content)

              this.total = response.data.totalElements;

            }).catch((error)=> {
              console.log(error);
            });
        }

      },*!/

     /!* hangzhouHover:function(){
        $("#hzs").addClass("moren");
        $("#hzs").removeClass("mospan");
        $("#bjs").removeClass("moren");
        $("#wxs").removeClass("moren");
        $("#wxs").addClass("mospan");
        $("#bjs").addClass("mospan");
        this.Asd=false;
        this.Ais = true;
        this.Sis=false;

      },*!/
     /!* recruitment:function(){
        this.isNotShow = false;
        this.isShow = true;
        $(".spanbot1").css({"borderBottom":"none","color":"#333333"});
        $(".spanbos1").css({"borderBottom":"2px solid #da121a","color":"#da121a"});
      },
      companyCulture:function(){
        this.isNotShow = true;
        this.isShow = false;
        $(".spanbos1").css({"borderBottom":"none","color":"#333333"});
        $(".spanbot1").css({"borderBottom":"2px solid #da121a","color":"#da121a"});
      },*!/
      wuxiHover:function(){
        $("#hzs").addClass("mospan");
        $("#hzs").removeClass("moren");
        $("#bjs").removeClass("moren");
        $("#wxs").removeClass("mospan");
        $("#wxs").addClass("moren");
        $("#bjs").addClass("mospan");
        this.Asd=false;
        this.Ais = false;
        this.Sis=true;

      },
      tiyans:function(){
        this.$router.push({path: '/login'});
      },
      xiaowei:function(){
        //  var that = this;
        //var win = window.open("#/CustomerService");
        //var win = window.open("http://xiaowei.io/chat/pc/index.html?appid=3311&style=red","_blank","height=600,width=500","top=0,left=0,toolbar=yes,menubar=yes,scrollbars=no,resizable=no,location=no,status=no");
         var win = window.open("#/CustomerService","_blank","height=600,width=500","toolbar=yes, location=no, directories=no, status=no, menubar=no, scrollbars=yes, resizable=no, copyhistory=yes");
      },
      phoneEnter:function(){
        this.phoneBox = true;
      },
      phoneleave:function(){
        this.phoneBox = false;
      },
      ctaCloundCsbs:function(){
        //window.open("http://demo.csb-china.com")
      },
      getAllRegion:function () {
        this.$this.get('broker/prop/typedata/recruit-place/-1').then((response)=>{

          this.regions = response.data.data;
          //console.log(this)

        }).catch((error)=>{})
      },
      getAllRecruit:function () {
        if(this.region!=''){
          this.$this.get('broker/recruit/getAllJob/'+this.region).then((response)=>{

            this.jobs = response.data;
            this.job = '';
            this.getprof();
            //console.log(this)

          }).catch((error)=>{})
        }else{
          this.getprof();
        }

      },
      getAllJobs:function(){
        this.getprof();
      }


    },
    mounted:function(){
     /!* this.getAllRegion();
      //this.getAllRecruit();
      this.getprof();*!/
      $(document).ready(function(){
        $(".spanbot1").css({"borderBottom":"2px solid #da121a","color":"#da121a"});
        $(".spanbot").css({"color":"#da121a"});
        $(window).scroll(function(){
          if($(this).scrollTop() > 550){
            $('.scrollUp').css("display","block")
          }else{
            $('.scrollUp').fadeOut();
          }
        });
        $(".scrollUp").click(function(){
          $('html ,body').animate({scrollTop: 0}, 300);
          return false;
        });

        // 图片轮播
        if(document.documentElement.clientWidth>=768){
          var deg=0;
          var images	= $('#stage img').removeClass('default').addClass('animationReady');
          var dim		= { width:images.width(),height:images.height()};
          var cnt = images.length;
          var centerX = $('#stage').width()/2;
          var centerY = $('#stage').height()/2 - dim.height/2;
          function rotate(step,total){
            deg+=step;
            var eSin,eCos,newWidth,newHeight,q;
            for(var i=0;i<cnt;i++){
              q = ((360/cnt)*i+deg)*Math.PI/180;
              eSin		= Math.sin(q);
              eCos		= Math.cos(q);
              q = (0.6+eSin*0.4);
              newWidth	= q*dim.width;
              newHeight	= q*dim.height;
              images.eq(i).css({
                top			: centerY+25*eSin,
                left		: centerX+300*eCos,
                opacity		: 0.8+eSin*0.2,
                marginLeft	: -newWidth/2,
                zIndex		: Math.round(80+eSin*20)
              }).width(newWidth).height(newHeight);
            }
            total-=Math.abs(step);
            if(total<=0) return false;
            setTimeout(function(){rotate(step,total)},40);
          }
          rotate(10,360/cnt);
          $('#phoneCarousel .previous').click(function(){
            rotate(-10,360/cnt);
          });
          $('#phoneCarousel .next').click(function(){
            rotate(10,360/cnt);
          });
          $('#phoneCarousel .previous,#phoneCarousel .next').hover(function(){
            clearInterval(timer);
          },function(){
            timer=setInterval(function(){rotate(10,360/cnt);},4000);
          });
          var timer=null;
          timer=setInterval(function(){rotate(10,360/cnt);},4000);

        }else {
          //$(".cloundzi").css("display","block");
          $(".defaimg").css({
            "width":"300px",
            "height":"200px"

          })
          $("#phoneCarousel").css({
            "width":"100%",
            "height":"100%"
          })
          $(".default").css({
            "left":"0",
            "margin-right":"auto",
            "margin-top":"0",
            "margin-bottom":"0",
            "margin-left":"auto",
            "position":"static"
          })
          $("previous arrow").css("display","none");
          $("next arrow").css("display","none");
          $("#stage img").css({

            "margin-right":"auto",
            "margin-top":"0",
            "margin-bottom":"0",
            "margin-left":"auto",

          })
          $("#stage img").css("display","block")
          $(".weiduduan").css("width","300px")
          $("#stage").css({
            "left":"0",
            "position":"static",
            "margin-left":"0px",
            "width":"100%"
          })
        }

      })
    }*/
  }
</script>
