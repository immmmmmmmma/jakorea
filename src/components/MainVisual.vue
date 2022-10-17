<template>
    <div class="mainVisual">
        <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper">
            <swiper-slide v-for="(item,i) in swiperView" :key="i" class="swiperWrap d-flex row">
                <div class="innerText col-12 col-md-6">
                    <h2 v-html="item.mainTitle"></h2>
                    <p v-html="item.subtitle"></p>
                    <button class="btn">자세히 보기<i class="fa-solid fa-arrow-right-long"></i></button>
                </div>
                <div class="videoPlayer col-12 col-md-6">
                    <video :src="`./images/01mainSlide_video/${item.mVideo}`" muted autoplay class="video"></video>
                </div>
            </swiper-slide>
        </swiper>
        <div class="btnWrap">
        <div class="prev">이전</div>
        <div class="next">다음</div>
        </div>
    </div>
</template>

<script>

// #E1EFF2
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
import "swiper/css/pagination";


// import required modules
import { Navigation,Pagination } from "swiper";

//swiper data
import mainsData from "@/data/01mainSlide.js"

export default {
    props:["mainsData"],
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
        modules: [Navigation,Pagination],
        swiperView:mainsData,
        swiperOptions:{
        loop:true,
        navigation:{
          nextEl:'.visual .next',
          prevEl:'.visual .prev',
        },
        pagination:{
          clickable:true,
          // type:'fra',
        },

      }
    };
  },
};
</script>

<style lang="scss">
@import url('../assets/style.css');
    .mainVisual{
        width: 100%;
        background: #E1EFF2;
        height: 745px;
        overflow: hidden;
    }

    .videoPlayer{
        margin-left: auto;
        .video{
            height: 745px;
            width: 100%;
        }
    }
    .swiperWrap{
    }
    .innerText{
        color: #285f74;
        position: absolute;
        left: 36%;
        transform: translateX(-50%);
        h2{
            font-size: 66px;
            font-weight: 200;
        }
        p{
            font-size: 18px;
            line-break: 28.8px;
        }
        span{
            font-weight: 700;
        }
    }
    
    @media (max-width: 768px){
        
    }
</style>