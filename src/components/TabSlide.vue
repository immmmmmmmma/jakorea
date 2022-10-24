<template>
  <div class="tapWrap">
    <swiper
      v-bind="swiperOptions1"
      :modules="modules1"
      class="mySwiper1 p-5">
        <swiper-slide v-if="tab==1" v-for="item in noData" :key="item" class="slide p-5" :class="{noData:tab=1}">
          <h4>{{item.name}}</h4>
          <div class="title" v-html="item.title"></div>
          <p v-html="item.content"></p>
        </swiper-slide>
        <swiper-slide v-if="tab==2" v-for="item in stData" :key="item" class="slide p-5" :class="{stData:tab=2}">
          <h4>{{item.name}}</h4>
           <div class="title">{{item.title}}</div>
           <p v-html="item.subtitle"></p>
        </swiper-slide>
        <swiper-slide v-if="tab==3" v-for="item in neData" :key="item" class="slide p-5" :class="{neData:tab=3}">
          <h4>{{item.name}}</h4>
           <div class="title">{{item.title}}</div>
           <p v-html="item.content"></p>
        </swiper-slide>
      </swiper>
      <div class="btnWrap">
        <div class="prev"><i class="fa-solid fa-arrow-left-long"></i></div>
        <div class="next"><i class="fa-solid fa-arrow-right-long"></i></div>
      </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Pagination,Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props:[
    "noData",
    "stData",
    "neData",
    "tab"
  ],
  setup() {
    return {
      modules1: [Navigation,Pagination],
      swiperOptions1:{
        breakpoints:{
          1200: {
            slidesPerView:3,
          },
          900: {
            slidesPerView:2,
          }
        },
        spaceBetween:30,
        loop:true,
        observer: true,
        observeParents: true,
         navigation:{
          nextEl:'.tapWrap .next',
          prevEl:'.tapWrap .prev',
        },
      }
    };
  },
};
</script>

<style lang="scss" scoped>
.tapWrap{
  position: relative;
  .btnWrap{
    width: 100%;
    position: absolute;
    display: flex; justify-content: space-between;
    top: 50%;
    z-index: 100;
    .next, .prev{
      color: #00a0af;
      font-size: 18px;
      position: relative;
      z-index: 1;
      transition: .3s;  
      width: 66px;
      height: 53px;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #fff; 
      border-radius: 30px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
      cursor: pointer;
      &:hover{
        background: #00a0af;
        color:#fff;

      }
      }
  }

}
.mySwiper1{
  height: 500px;
.slide{
    width: 100px; 
    height: 100%;
    h4{
        background: #000;
        color: #fff;
        width: 80px;
        height: 30px;
        font-size: 0.7vw;
        display: flex; 
        justify-content: center;
        align-items: center;
        border-radius: 50px;
    }
    .title{
      font-weight: bold; 
      font-size: 1.3vw;
      height: 80px;
      overflow: hidden;
      text-overflow: hidden;
      }
    p{
      text-overflow: hidden; 
      overflow: hidden;
      height: 93px; 
      }
    }
}

</style>