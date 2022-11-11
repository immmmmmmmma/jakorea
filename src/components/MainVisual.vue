<template>
    <div class="mainVisual">
        <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper">
            <swiper-slide v-for="(item,i) in swiperView" :key="i" class="swiperWrap">
                <div class="container">
                    <div class="row">
                        <div class="innerText col-12 col-md-6 mv">
                            <div class="innerBox">
                                <h2 v-html="item.mainTitle"></h2>
                                <p v-html="item.subtitle"></p>
                                <button class="btn">
                                    <span>
                                    자세히 보기<i class="fa-solid fa-arrow-right-long"></i>
                                    </span>
                                    <div class="gradient"></div>
                                </button>
                            </div>
                        </div>
                        <div class="videoPlayer col-12 col-md-6">
                            <video :src="`./images/01mainSlide_video/${item.mVideo}`" muted autoplay class="video"></video>
                        </div>
                    </div>
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
@media (max-width: 768px){
      .mainVisual{
        height: initial;
      }  
    }    

    .videoPlayer{
        margin-left: auto;
        .video{
            height: 745px;
            width: 100%;
        }
    }
    .innerText{
        &.mv{
            display: flex;
            flex-direction: column;
            align-items:flex-start;
            justify-content: center;
            // justify-self: start;
    
            h2{
                color: #285f74;
                font-size: 66px;
                font-weight: 200;
                span{
                    font-weight: 700;
                }
            }
            p{
                color: #285f74;
                font-size: 18px;
                line-break: 28.8px;
            }
        }
    }
    .btn{
        margin-top: 85px;
        position: relative;
        padding: 22px 35px !important;
        border-radius: 40px !important;
        overflow: hidden;
        display: inline-block !important;
        box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
        transition: .3s !important;
        background: #fff;
        span{
            font-weight: 700;
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
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
            position: absolute;
            top: 0;
            left: 0;
            opacity: 0;
            transition: .3s;
            background-size: 1000%;
        }
        &:hover .gradient{
            animation: gradient 10s linear infinite;
            opacity: 1;
        }
    }
    
    @keyframes gradient {
     0% { background-position: 0% 50%; } 
     50% { background-position: 100% 50%; } 
     100% { background-position: 0% 50%; } 
     }
    @media (max-width: 768px){
        
    }
</style>
<style lang="scss" scoped>
    .btn{
        background: #fff;
        &:hover{
            background: none;
        }
    }
</style>