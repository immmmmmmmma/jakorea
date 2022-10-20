<template>
    <Swiper
    v-bind="swiperOptions1"
    :modules="modules1"
    class="mySwiper1">
        <swiper-slide v-if="tab==1" v-for="item in noData" :key="item" :class="{noData:tab=1}">
            <h4></h4> 
        </swiper-slide>

        <swiper-slide v-if="tab==2" v-for="item in stData" :key="item" :class="{stData:tab=2}">
            <h4></h4>
        </swiper-slide>

         <swiper-slide v-if="tab==3" v-for="item in neData" :key="item" :class="{neData:tab=3}">
            <h4></h4>
        </swiper-slide>
    </Swiper>

</template>

<script>
  import { Swiper, SwiperSlide } from "swiper/vue";

  import "swiper/css";
  
  import "swiper/css/pagination";
  import "swiper/css/navigation";
  
  import { Pagination, Navigation } from "swiper";
export default {
    components:{
        Swiper,
        SwiperSlide,
    },
    props:[
        "noData",
        "stData",
        "neData",
        "tab",
    ],
    setup(){
        return{
            modules1:[Pagination, Navigation],
            swiperOpaions1:{
                slidesPerView:3,
                spaceBetween:30,
                loop:true,
                observer: true,
                observeParents: true,
            }
        }
    }
}
</script>

<style lang="scss">
    .swiper-slide{
        height: 400px;
    }
</style>