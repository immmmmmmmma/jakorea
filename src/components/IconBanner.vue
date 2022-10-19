<template>
    <div class="iconBannerWrap">
        <div class="iconBanner"
        v-for="(item,i) in ibData" :key="i">
            <div class="iconBox">
                <img :src="`./images/02iconBanner/${item.src}`" alt="">
                <h2 v-html="item.title"></h2>
                <p v-html="item.subtitle"></p>
            </div>
        </div>
    </div>
</template>

<script>
// import { onMounted } from "vue";
// import AOS from "aos";
export default {    
    props:["ibData"],
}

// onMounted(() => {
//     AOS.init();
// })
</script>

<style lang="scss">

@import url('../assets/style.css');
.iconBannerWrap{
    display: flex;
    width: 1400px;
    margin: 0 auto;
}
.iconBanner{
    .iconBox{
        width: 280px;
        height: 333px;
        padding: 40px 25px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        img{
            height: 140px;
            transition: 0.3s;
            margin-bottom: 20px;
        }
        h2{
            font-size: 18px;
            font-weight: 700;
            text-align: center;
            margin-bottom: 20px;
        }
        p{
            font-size: 15px;
            text-align: center;
        }
        &:hover img{
            transform: translateY(-20px);
        }
    }
}
</style>