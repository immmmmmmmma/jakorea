<template>
    <div class="mainVisual">
        <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper">
            <swiper-slide v-for="(item,i) in swiperView" :key="i" class="swiperWrap d-flex row">
                <div class="innerText col-12 col-md-6">
                    <h2 v-html="item.mainTitle"></h2>
                    <p v-html="item.subtitle"></p>
                    <button class="btn">
                        <span>
                        자세히 보기<i class="fa-solid fa-arrow-right-long"></i>
                        </span>
                        <div class="gradient"></div>
                    </button>
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
        top: 20%;
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
        .btn{
            margin-top: 85px;
            position: relative;
            padding: 22px 35px;
            border-radius: 40px;
            overflow: hidden;
            display: inline-block;
            background: #fff;
            box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
            transition: .3s;
            span{
                z-index: 3;
                i{
                    margin-left: 48px;
                }
            }
            &:hover span{
                color: #fff;
            }
            .gradient{
                z-index: -1;
                width: 100%;
                height: 100%;
                background-image: linear-gradient( -45deg,#00a0af,#00c0ca, #008b9c, #28708b,#285f74, #22404d,#285f74,#28708b, #008b9c,#00c0ca,#00a0af) !important;
                position: absolute;
                top: 0;
                left: 0;
                opacity: 0;
                transition: .3s;
                background-size: 1000%;
            }
            &:hover .gradient{
                animation: animate 10s linear infinite;
                opacity: 1;
            }
        }
    }
    
    @keyframes animate{

    }
    @media (max-width: 768px){
        
    }
</style>