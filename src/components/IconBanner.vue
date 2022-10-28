<template>
    <div class="iconBannerWrap container">
        <div class="iconBanner row"
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
    margin: 0 auto;
    margin-bottom: 100px;
}
.iconBanner{
    margin: 0 auto;
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
@media (max-width: 768px){
    .iconBannerWrap{
        overflow: hidden;
    }
.iconBox{
    p{
        display: none;
    }
}
}    
</style>
