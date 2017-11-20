<template>
  <div class="wrap">
    <div class="header">
       <div class="NavHeader">
         <div class="nav" v-on:mouseover="showDetail">
           <div :class="{nav1:active ,nav2:unActive}"></div>
           <div :class="{nav1:active ,nav2:unActive}"></div>
           <div :class="{nav1:active ,nav2:unActive}"></div>
           <div :class="{total:active ,total1:unActive}">全部</div>
         </div>
         <div class="logo">
           <img src="./logo.png" alt="">
         </div>
         <div class="list">
           <ul class="listUl">
             <li class="listLi"  v-on:mouseover="showA1" v-on:mouseleave="hiddenlistB1">
               <a href="" :class="{listA:isshowA1,listB:isshowB1}">主页</a>
             </li>
             <li class="listLi" v-on:mouseover="showA2" v-on:mouseleave="hiddenlistB2" >
               <a href="" :class="{listA:isshowA2,listB:isshowB2}">房产行业</a>
             </li>
             <li class="listLi" v-on:mouseover="showA3" v-on:mouseleave="hiddenlistB3">
               <a href="" :class="{listA:isshowA3,listB:isshowB3}">企业数据</a>
             </li>
             <li class="listLi" v-on:mouseover="showA4" v-on:mouseleave="hiddenlistB4">
               <a href="" :class="{listA:isshowA4,listB:isshowB4}">旅游行业</a>
             </li>
             <li class="listLi" v-on:mouseover="showA5" v-on:mouseleave="hiddenlistB5">
               <a href="" :class="{listA:isshowA5,listB:isshowB5}">医疗行业</a>
             </li>
             <li class="listLi" v-on:mouseover="showA6" v-on:mouseleave="hiddenlistB6">
               <a href="" :class="{listA:isshowA6,listB:isshowB6}">生活常用</a>
             </li>
           </ul>
           <div :class="{bar1:isbar1,bar2:isbar2,bar3:isbar3,bar4:isbar4,bar5:isbar5,bar6:isbar6}">
         </div>
         </div>
         <div class="inP" v-on:mouseover="showInput" v-on:mouseleave="hiddenInput">
           <input :class="{input1:uninpActive ,input2:inpActve}" type="text">
           <img src="./search.png" alt="">
         </div>
         <div class="btn" v-on:mouseover="showImg2" v-on:mouseleave="showImg1">
           <img v-bind:src="btnImg" alt="">
         </div>

       </div>
       <div class="downWrap" v-show="isshow"  v-on:mouseleave="hiddenDetail" >
         <div class="down">
           <div class="Downlist">
           <ul class="dropDownUl" >
             <li class="dropDownLi" v-on:mouseover="showMenu1" v-on:mouseleave="hiddenMenu1">
               <a :class="{menuA:isMenuA1,unMenuA:isunMenuA1}" href="">
               数据
               </a>
               <span :class="{menuSpan1:isspan1,menuSpan2:isunspan1}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu2" v-on:mouseleave="hiddenMenu2">
               <a :class="{menuA:isMenuA2,unMenuA:isunMenuA2}" href="">
               房产行业
               </a>
               <span :class="{menuSpan1:isMenuA2,menuSpan2:isunMenuA2}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu3" v-on:mouseleave="hiddenMenu3">
               <a :class="{menuA:isMenuA3,unMenuA:isunMenuA3}" href="">
                 企业数据
               </a>
               <span :class="{menuSpan1:isMenuA3,menuSpan2:isunMenuA3}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu4" v-on:mouseleave="hiddenMenu4">
               <a :class="{menuA:isMenuA4,unMenuA:isunMenuA4}" href="">
                 企业数据
               </a>
               <span :class="{menuSpan1:isMenuA4,menuSpan2:isunMenuA4}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu5" v-on:mouseleave="hiddenMenu5">
               <a :class="{menuA:isMenuA5,unMenuA:isunMenuA5}" href="">
               旅游行业
               </a>
               <span :class="{menuSpan1:isMenuA5,menuSpan2:isunMenuA5}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu6" v-on:mouseleave="hiddenMenu6">
               <a :class="{menuA:isMenuA6,unMenuA:isunMenuA6}" href="">
               医疗行业
               </a>
               <span :class="{menuSpan1:isMenuA6,menuSpan2:isunMenuA6}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu7" v-on:mouseleave="hiddenMenu7">
               <a :class="{menuA:isMenuA7,unMenuA:isunMenuA7}" href="">
               生活常用
               </a>
               <span :class="{menuSpan1:isMenuA7,menuSpan2:isunMenuA7}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu8" v-on:mouseleave="hiddenMenu8">
               <a :class="{menuA:isMenuA8,unMenuA:isunMenuA8}" href="">
               汽车行业
               </a>
               <span :class="{menuSpan1:isMenuA8,menuSpan2:isunMenuA8}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu9" v-on:mouseleave="hiddenMenu9">
               <a :class="{menuA:isMenuA9,unMenuA:isunMenuA9}" href="">
               合作与生态
               </a>
               <span :class="{menuSpan1:isMenuA9,menuSpan2:isunMenuA9}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu10" v-on:mouseleave="hiddenMenu10">
               <a :class="{menuA:isMenuA10,unMenuA:isunMenuA10}" href="">
               云市场
               </a>
               <span :class="{menuSpan1:isMenuA10,menuSpan2:isunMenuA10}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu11" v-on:mouseleave="hiddenMenu11">
               <a :class="{menuA:isMenuA11,unMenuA:isunMenuA11}" href="">
               支持
               </a>
               <span :class="{menuSpan1:isMenuA11,menuSpan2:isunMenuA11}">&gt;</span>
             </li>
             <li class="dropDownLi" v-on:mouseover="showMenu12" v-on:mouseleave="hiddenMenu12">
               <a :class="{menuA:isMenuA12,unMenuA:isunMenuA12}" href="">
               开发者中心
               </a>
               <span :class="{menuSpan1:isMenuA12,menuSpan2:isunMenuA12}">&gt;</span>
             </li>
           </ul>
           <div class="linew">
           </div>
           <div class="tel">
             <img src="./tel.png" alt="">
             010-57817778
           </div>
         </div>
         </div>
       </div>
     </div>

    <div class="content">
      <div class="swpWrap">
        <div class="swp">
          <el-carousel height="520px" :interval="2000" arrow="always" class="swipe">
            <el-carousel-item v-for="item in 1" :key="item">
              <h3>
                <img width="100%" src="./swipe1.png" alt="">
              </h3>
            </el-carousel-item>
            <el-carousel-item v-for="item in 1" :key="item">
              <h3>
                <img  width="100%" src="./swipe1.png" alt="">
              </h3>
            </el-carousel-item>
            <el-carousel-item v-for="item in 1" :key="item">
              <h3>
                <img width="100%" src="./swipe1.png" alt="">
              </h3>
            </el-carousel-item>
          </el-carousel>
        </div>
      </div>
      <div class="line">
        <div class="lineWrap">
          <div class="line1">
            <img src="./line1.png" alt="">
          </div>
          精品数据
          <div class="line2">
            <img src="./line2.png" alt="">
          </div>
        </div>
      </div>
      <div class="container">
        <ul class="containerUl">
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg"  src="./22.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
        </ul>
      </div>
      <div class="whi">
      </div>
      <div class="btnWrap">
        <div class="btn" >
          <button :class="{btnunActive:BtnunActive1 ,btnActive:BtnActive1}" v-on:mouseover="showBigbtn1" v-on:mouseleave="hiddenBigbtn1">
            查看全部
          </button>
        </div>
      </div>
      <div class="line">
        <div class="lineWrap">
          <div class="line1">
            <img src="./line1.png" alt="">
          </div>
          热门数据
          <div class="line2">
            <img src="./line2.png" alt="">
          </div>
        </div>
      </div>
      <div class="container">
        <ul class="containerUl">
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg"  src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg"  src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
          <li class="containerLi">
            <a href="">
              <img class="containerLiimg" src="./11.png" alt="">
              <p class="containerzi">
                <img src="./logo1.png" alt="">
                全国旅游景点数据
              </p>
            </a>
          </li>
        </ul>
      </div>
      <div class="whi">
      </div>
      <div class="btnWrap">
        <div class="btn"  >
          <button :class="{btnunActive:BtnunActive2 ,btnActive:BtnActive2}" v-on:mouseover="showBigbtn2" v-on:mouseleave="hiddenBigbtn2">
            查看全部
          </button>
        </div>
      </div>
      <div class="whi">
      </div>
    </div>
    <div class="footer">
      <div class="footerContent">
        <div class="footerLeft">
          <p class="relation">
            <img src="./relation.png" alt="">
            联系我们
          </p>
          <p class="address">
            <img src="./addss.png" alt="">
            北京东城区和平里东滨河路乙1号雍和航行园8号楼3层
          </p>
          <p class="telephone">
            <img src="./tele.png" alt="">
            杨仁慧(183 1030 8102)
          </p>
          <p class="post">
            <img src="./post.png" alt="">
            100013
          </p>
        </div>
        <div class="footerCenter">
          <p class="mailbox">
            <img src="./mailbox.png" alt="">
            xiaof.jin@hnair.com
          </p>
          <p class="faxes">
            <img src="./faxes.png" alt="">
            010-57817778
          </p>
          <p class="phone">
            <img src="./phone.png" alt="">
            010-57817778
          </p>
        </div>
        <div class="footerRight">
          <img src="./qr.png" alt="">
        </div>
        <div class="line2">
        </div>
        <div class="statement">
          <div class="copy"> © Copyright 2017-All rights reserved Designed by HooThemes</div>
          <div class="point">
            <a href="javascript:scroll(0,0)" class="pointA">
              <img src="./back.png" alt="">
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data () {

      return {
        active:false,
        unActive:true,
        isshow:false,
        uninpActive:true,
        inpActve:false,
        btnImg:require("./btn1.png"),
        BtnunActive1:true,
        BtnActive1:false,
        BtnunActive2:true,
        BtnActive2:false,
        isshowA1:true,
        isshowB1:false,
        isshowA2:true,
        isshowB2:false,
        isshowA3:true,
        isshowB3:false,
        isshowA4:true,
        isshowB4:false,
        isshowA5:true,
        isshowB5:false,
        isshowA6:true,
        isshowB6:false,
        isbar1:false,
        isbar2:false,
        isbar3:false,
        isbar4:false,
        isbar5:false,
        isbar6:false,
        isMenuA1:true,
        isunMenuA1:false,
        isspan1:true,
        isunspan1:false,
        isMenuA2:true,
        isunMenuA2:false,
        isspan2:true,
        isunspan2:false,
        isMenuA3:true,
        isunMenuA3:false,
        isspan3:true,
        isunspan3:false,
        isMenuA4:true,
        isunMenuA4:false,
        isspan4:true,
        isunspan4:false,
        isMenuA5:true,
        isunMenuA5:false,
        isspan5:true,
        isunspan5:false,
        isMenuA6:true,
        isunMenuA6:false,
        isspan6:true,
        isunspan6:false,
        isMenuA7:true,
        isunMenuA7:false,
        isspan7:true,
        isunspan7:false,
        isMenuA8:true,
        isunMenuA8:false,
        isspan8:true,
        isunspan8:false,
        isMenuA9:true,
        isunMenuA9:false,
        isspan9:true,
        isunspan9:false,
        isMenuA10:true,
        isunMenuA10:false,
        isspan10:true,
        isunspan10:false,
        isMenuA11:true,
        isunMenuA11:false,
        isspan11:true,
        isunspan11:false,
        isMenuA12:true,
        isunMenuA12:false,
        isspan12:true,
        isunspan12:false
      }
    },
    methods:{
      showDetail(){
        this.isshow = true
        this.active = true
        this.unActive = false
      },
      hiddenDetail(){
        this.isshow = false
        this.active = false
        this.unActive = true
      },
      showInput(){
        this.inpActve = true
        this.uninpActve = false
      },
      hiddenInput(){
        this.inpActve = false
        this.uninpActve = true
      },
      showImg2(){
        this.btnImg = require("./btn2.png")
      },
      showImg1(){
        this.btnImg = require("./btn1.png")
      },
      showBigbtn1(){
        this.BtnunActive1 = false
        this.BtnActive1 =true
      },
      hiddenBigbtn1(){
        this.BtnunActive1 = true
        this.BtnActive1 = false
      },
      showBigbtn2(){
        this.BtnunActive2 = false
        this.BtnActive2 =true
      },
      hiddenBigbtn2(){
        this.BtnunActive2 = true
        this.BtnActive2 = false
      },
      shiftin(){
        this.isshow = true
      },
      showA1(){
        this.isbar1 = true
        this.isshowA1 = false
        this.isshowB1=true
      },
      hiddenlistB1(){
        this.isbar1 = false
        this.isshowA1 = true
        this.isshowB1=false
      },
      showA2(){
        this.isbar2 = true
        this.isshowA2 = false
        this.isshowB2=true
      },
      hiddenlistB2(){
        this.isbar2 = false
        this.isshowA2 = true
        this.isshowB2=false
      },
      showA3(){
        this.isbar3 = true
        this.isshowA3 = false
        this.isshowB3=true
      },
      hiddenlistB3(){
        this.isbar3 = false
        this.isshowA3 = true
        this.isshowB3= false
      },
      showA4(){
        this.isbar4= true
        this.isshowA4 = false
        this.isshowB4=true
      },
      hiddenlistB4(){
        this.isbar4= false
        this.isshowA4 = true
        this.isshowB4=false
      },
      showA5(){
        this.isbar5 = true
        this.isshowA5 = false
        this.isshowB5=true
      },
      hiddenlistB5(){
        this.isbar5 = false
        this.isshowA5 = true
        this.isshowB5=false
      },
      showA6(){
        this.isbar6 = true
        this.isshowA6 = false
        this.isshowB6=true
      },
      hiddenlistB6(){
        this.isbar6= false
        this.isshowA6 = true
        this.isshowB6=false
      },
      showMenu1(){
        this.isMenuA1= false
        this.isunMenuA1= true
        this.isspan1 = false
        this.isunspan1 = true
      },
      hiddenMenu1(){
        this.isMenuA1= true
        this.isunMenuA1= false
        this.isspan1 = true
        this.isunspan1 = false
      },
      showMenu2(){
        this.isMenuA2= false
        this.isunMenuA2= true
        this.isspan2 = false
        this.isunspan2= true
      },
      hiddenMenu2(){
        this.isMenuA2= true
        this.isunMenuA2= false
        this.isspan2 = true
        this.isunspan2 = false
      },
      showMenu3(){
        this.isMenuA3= false
        this.isunMenuA3= true
        this.isspan3 = false
        this.isunspan3 = true
      },
      hiddenMenu3(){
        this.isMenuA3= true
        this.isunMenuA3= false
        this.isspan3 = true
        this.isunspan3 = false
      },
      showMenu4(){
        this.isMenuA4= false
        this.isunMenuA4= true
        this.isspan4 = false
        this.isunspan4 = true
      },
      hiddenMenu4(){
        this.isMenuA4= true
        this.isunMenuA4= false
        this.isspan4 = true
        this.isunspan4= false
      },
      showMenu5(){
        this.isMenuA5= false
        this.isunMenuA5= true
        this.isspan5 = false
        this.isunspan5 = true
      },
      hiddenMenu5(){
        this.isMenuA5= true
        this.isunMenuA5= false
        this.isspan5 = true
        this.isunspan5= false
      },
      showMenu6(){
        this.isMenuA6= false
        this.isunMenuA6= true
        this.isspan6 = false
        this.isunspan6 = true
      },
      hiddenMenu6(){
        this.isMenuA6= true
        this.isunMenuA6= false
        this.isspan6 = true
        this.isunspan6= false
      },
      showMenu7(){
        this.isMenuA7= false
        this.isunMenuA7= true
        this.isspan7 = false
        this.isunspan7 = true
      },
      hiddenMenu7(){
        this.isMenuA7= true
        this.isunMenuA7= false
        this.isspan7 = true
        this.isunspan7= false
      },
      showMenu8(){
        this.isMenuA8= false
        this.isunMenuA8= true
        this.isspan8 = false
        this.isunspan8 = true
      },
      hiddenMenu8(){
        this.isMenuA8= true
        this.isunMenuA8= false
        this.isspan8 = true
        this.isunspan8= false
      },
      showMenu9(){
        this.isMenuA9= false
        this.isunMenuA9= true
        this.isspan9 = false
        this.isunspan9 = true
      },
      hiddenMenu9(){
        this.isMenuA9= true
        this.isunMenuA9= false
        this.isspan9 = true
        this.isunspan9= false
      },
      showMenu10(){
        this.isMenuA10= false
        this.isunMenuA10= true
        this.isspan10 = false
        this.isunspan10 = true
      },
      hiddenMenu10(){
        this.isMenuA10= true
        this.isunMenuA10= false
        this.isspan10 = true
        this.isunspan10= false
      },
      showMenu11(){
        this.isMenuA11= false
        this.isunMenuA11= true
        this.isspan11 = false
        this.isunspan11 = true
      },
      hiddenMenu11(){
        this.isMenuA11= true
        this.isunMenuA11= false
        this.isspan11 = true
        this.isunspan11= false
      },
      showMenu12(){
        this.isMenuA12= false
        this.isunMenuA12= true
        this.isspan12 = false
        this.isunspan12 = true
      },
      hiddenMenu12(){
        this.isMenuA12= true
        this.isunMenuA12= false
        this.isspan12 = true
        this.isunspan12= false
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
/*@media screen and (min-width: 750px)*/
  .wrap
    width 100%
    .header
      width 100%
      height 95px
      background: #0d4285
      .NavHeader
        position relative
        width 100%
        min-width 1200px
        height 100%
        margin 0 auto
        .nav
          position relative
          left 3.46%
          top 34px
          width 6.73%
          height 32px
          .nav1
            width 33.3%
            height 4px
            background: #77d2dd
            margin-bottom 7px
          .nav2
            width 33.3%
            height 4px
            background: #fff
            margin-bottom 7px
          .total
            position absolute
            left 44.4%
            top 1px
            font-size 22px
            color: #77d2dd;
          .total1
            position absolute
            left 44.4%
            top 1px
            font-size 22px
            color: #fff;
        .logo
          width 12.6%
          height 40px
          position absolute
          left 11%
          top 30px
          &>img
           width 100%
        .list
          width 527px
          height 30px
          position absolute
          left 24%
          top 36px
          .listUl
            width:100%
            height:100%
            background:#0d4285
            .listLi
              display:inline;
              height:100%
              .listA
                display:inline-block;
                padding:0 8px;
                height:30px;
                line-height:30px;
                font-size:18px
                color:#FFF;
              .listB
                display:inline-block;
                padding:0 8px;
                height:30px;
                line-height:30px;
                font-size:18px
                color:#91f8f8;
          .bar1
            width 70px
            height 2px
            background: #91f8f8;
            position absolute
            left -10px
            top 57px
          .bar2
            width 70px
            height 2px
            background: #91f8f8;
            position absolute
            left 65px
            top 57px
          .bar3
            width 70px
            height 2px
            background: #91f8f8;
            position absolute
            left 159px
            top 57px
          .bar4
            width 70px
            height 2px
            background: #91f8f8;
            position absolute
            left 251px
            top 57px
          .bar5
            width 70px
            height 2px
            background: #91f8f8;
            position absolute
            left 343px
            top 57px
          .bar6
            width 70px
            height 2px
            background: #91f8f8;
            position absolute
            left 435px
            top 57px


        .inP
          width 19%
          height 46px
          position absolute
          left 67%
          top 26px
          &>img
            position absolute
            right 8px
            top 16px
          .input1
            border-radius 40px
            width 100%
            height 100%
            background: #0d4285;
            border 0px
            outline none
          .input2
            border-radius 40px
            width 100%
            height 100%
            background: #0d4285;
            border 1px solid #4872ab
            outline none
        .btn
          width 128px
          height 44px
          position absolute
          left 87.50%
          top 25.5px
      .downWrap
        width 100%
        height 520px
        .down
          width 100%
          margin 0 auto
          .Downlist
            opacity 0.7
            background: #062445;
            width 233px
            height 520px
            z-index 110
            position absolute
            .dropDownUl
              width 100%
              height 100%
              padding-top 6px
              .dropDownLi
                padding-left 45px
                color #FFF
                width 100%
                height 37px
                font-size 15px
                line-height 37px
                .menuA
                  color #FFF
                .unMenuA
                  color #00a4ff
                .menuSpan1
                  color #FFF
                  position absolute
                  right 30px
                .menuSpan2
                  color #00a4ff
                  position absolute
                  right 30px
            .linew
              position absolute
              left 17px
              bottom 57px
              width 85%
              height 1px
              background: #365879;
            .tel
              position absolute
              bottom 15px
              left 45px
              width 100%
              height 21px
              color #fff
              &>img
                vertical-align middle
    .content
      width 100%
      .swpWrap
        width 100%
        .swp
          width 100%
          margin 0 auto
          &>img
            float left
            width 100%
            height 100%
      .line
        width 100%
        height 136px
        .lineWrap
          width 392px
          height 136px
          font-size 25px
          position relative
          text-align center
          margin 0 auto
          line-height 136px
          .line1
            position absolute
            top 0px
            left 5px
          .line2
            position absolute
            top -2px
            left 262px
      .container
        width 100%
        .containerUl
          margin 0 auto
          overflow hidden
          width:93%;
          min-width 1200px
          .containerLi
            border 1px solid #dad9d9
            float left
            width 23.2%
            overflow hidden
            display block
            margin-left 0.785%
            margin-right 0.785%
            margin-bottom 20px
            &>a
              text-align center
              display block
              width 100%
              height 100%
              .containerLiimg
                width 100%
              .containerzi
                padding-top 6%
                padding-bottom 6%
                color #121212
                &>img
                  vertical-align middle
      .whi
        width 100%
        height 54px

      .btnWrap
        width 100%
        height 55px
        border 0
        .btn
          margin 0 auto
          text-align center
          width 93.78%
          height 100%
          .btnunActive
            width 242px
            height 100%
            border-radius 50px
            border 1px solid #9d9d9d
            background: #fff
            color #9d9d9d
            font-size 23px
            outline none
          .btnActive
            width 242px
            height 100%
            border hidden
            border-radius 50px
            background: #00a4ff
            color #e9f4ff
            font-size 23px
            outline none
    .footer
      width 100%
      height 482px
      background: url("./bg.jpg") no-repeat  ;
      background-size: 100% 482px;
      .footerContent
        padding-left 3.11%
        padding-right 3.11%
        width 93.78%
        min-width 1200px
        height 100%
        margin 0 auto
        .footerLeft
          float left
          width 44.7%
          height 385px
          .relation
            font-size 25px
            color #fff
            margin-left 60px
            margin-top 50px
            &>img
              vertical-align middle
          .address
            margin-left 60px
            margin-top 50px
            font-size 20px
            color #fff
            &>img
              vertical-align middle
          .telephone
            margin-left 60px
            margin-top 50px
            font-size 20px
            color #fff
            &>img
              vertical-align middle
          .post
            margin-left 60px
            margin-top 50px
            font-size 20px
            color #fff
            &>img
              vertical-align middle

        .footerCenter
          float left
          width 35.9%
          height 167px
          .mailbox
            font-size 20px
            line-height 20px
            color #fff
            margin-left 60px
            margin-top 159px
            &>img
              vertical-align middle
          .faxes
            margin-left 60px
            margin-top 50px
            font-size 20px
            color #fff
            &>img
              vertical-align middle
          .phone
            margin-left 60px
            margin-top 50px
            font-size 20px
            line-height 20px
            color #fff
            &>img
              vertical-align middle
        .footerRight
          margin-top 60px
          float right
          width 19.4%
          height 385px
        .line2
          position relative
          top 385px
          left 15px
          width 98%
          height 2px
          background: #7c8491;
        .statement
          text-align center
          width 100%
          height 20px
          position relative
          top 385px
          .copy
            position absolute
            top 40px
            left 345px
            font-size 20px
            line-height 20px
            color #fff
          .point
            position absolute
            top 30px
            right 80px
            .pointA
              width 100%
</style>
