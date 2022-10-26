<template>

  <div class="EduSlide">
        <div class="container">
            <h1 class="mb-2 eduH">JA 교육 프로그램</h1>
            <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper">
                <swiper-slide v-for="(item,i) in swiperView" :key="i" class="swiperWrap edu row">
                    <div class="innerText col-12 col-md-6">
                        <h2 v-html="item.title"></h2>
                        <p v-html="item.subtitle"></p>
                        <button class="btn edu">
                            <span>
                            자세히 보기<i class="fa-solid fa-arrow-right-long"></i>
                            </span>
                            <div class="gradient"></div>
                        </button>
                    </div>
                    <div class="eduImg col-12 col-md-6">
                        <img :src="`./images/03eduProgram/${item.src}`" alt="">
                    </div>
                </swiper-slide>
            </swiper>
        </div>
        <div class="btnWrap edu">
            <div class="prev"><i class="fa-solid fa-arrow-left-long"></i></div>
            <div class="next"><i class="fa-solid fa-arrow-right-long"></i></div>
        </div>
        <div class="eduAcc"></div>
    </div>
</template>

<script>

import { Swiper, SwiperSlide } from "swiper/vue";


import "swiper/css";

import "swiper/css/navigation";


import { Navigation} from "swiper";

import epData from "@/data/03eduProgram.js"

export default {
    props:["epData"],
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
        modules: [Navigation],
        swiperView:epData,
        swiperOptions:{
        loop:true,
        navigation:{
          nextEl:'.btnWrap .next',
          prevEl:'.btnWrap .prev',
        },


      }
    };
  },
};




</script>

<style lang="scss">
.EduSlide{
    position: relative;
}
.eduH{
    font-weight: 700;
}
.swiperWrap.edu{

    .innerText{
        display: flex;
        justify-content: center;
        align-content: center;
        flex-direction: column;
        padding: 0 40px;
        color: #333;
        h2{
            line-height: 45px;
            font-size: 35px;
            font-weight: 700;

        }

    }
}
.eduImg{
    height: 505px;
    padding: 0 200px 0 0;
    img{
        height: 417px;
    }
}
.eduAcc{
    position: absolute;
    top: 0;
    left: 1410px;
    width: 520px;
    height: 100%;
    border-top-left-radius: 50px;
    background: #F3F6F7;
}
.btnWrap{
    &.edu{

        .next,.prev{
            font-size: 45px;
            color: #cacaca;
            position: absolute;
            z-index: 999;
        }
        .prev{
            top: 230px;
            left: 240px;
        }
        .next{
            top: 230px;
            right: 240px;
        }
    }
}
.btn{
    &.edu{
        width: 220px;

    }
}

</style>