<template>
  <div class="wrap Main09Sponsor">
    <div class="container">
      <div class="row">
        <div class="col-md-4 txt">
            <p>국내외 여러기업이 동참하고 있습니다.</p>
            <h2>JA Korea 후원</h2>
                <button class="btn">
                    <span>
                    자세히 보기<i class="fa-solid fa-arrow-right-long"></i>
                    </span>
                    <div class="gradient"></div>
                </button>
            <div class="paging d-flex gap-3 ">  
                <div class="prev"><i class="fa-solid fa-arrow-left-long"></i></div>
                <div class="next"><i class="fa-solid fa-arrow-right-long"></i></div>            
            </div>
        </div>
        <div class="col-md-8" style="height:400px">
            <swiper            
                :modules="modules2"
                v-bind="swiperOptions2" 
                class="mySwiper03"
            > 
            <swiper-slide  v-for="(item, i) in suData" :key="i">
              <ul class="wrapImgBg">
                <li>
                    <div class="wrapImg">
                        <img :src="`images/09support/${item.src}`" alt="" class="suImg">
                    </div>
                </li>
              </ul>
            </swiper-slide>
          </swiper>
        </div>
      </div>
    </div>
  </div>      
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/grid";
import "swiper/css/navigation";


// import required modules
import { Grid, Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules2: [Grid, Navigation],
       swiperOptions2:{
        slidesPerView:3,
        grid:{
              rows: 3,
            },
        spaceBetween:10,
        navigation:{
          nextEl:'.paging .next',
          prevEl:'.paging .prev',
        },   
      }

  
    };   
  },
   props :["suData"],
};
</script>

<style lang="scss">
.Main09Sponsor{
  margin-bottom: 180px;
}
    .txt{
        position: relative;
        p{
            font-size: 17;
            font-weight: 700;
            color: #285F74;
        }
        h2{
            font-weight: 700;
            font-size: 45px;
        }

    }
    .wrapImgBg{
        display: flex;
        flex-wrap: wrap;
        li{
            width: 100%;
            margin-right: 30px;
            margin-bottom: 26px;
            overflow: hidden;
            border-radius: 8px;
        .wrapImg{
            padding-top: 35%;
            position: relative;
            background: #f3f6f7;
        }
        }
    }
    .suImg{
        max-height: 38%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        max-width: 70%;
    }
.swiper-grid-column>.swiper-wrapper {
    flex-wrap: wrap;
    flex-direction: row;
    }
    .paging .next,.paging .prev{
        position: absolute;
        top: 340px;
        font-size: 35px;
        font-weight: 300;
        line-height: 35px;
        color: #cacaca;
        transition: 0.3s;
        &:hover{
            color: #333;
        }
    }
    .paging .next{
        left: 180px;
    }
    .paging .prev{
        left: 10px;
    }
</style>