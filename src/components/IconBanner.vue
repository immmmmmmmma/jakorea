<template>
    <div class="iconBanner"
    v-for="(item,i) in ibData" :key="i">
        <img :src="`./images/02iconBanner/${item.src}`" alt="">
        <h2 v-html="item.title"></h2>
        <p v-html="item.subtitle"></p>
    </div>
    sadafaf
</template>

<script>

export default {    
    props:["ibData"],
}
</script>

<style>
@import url('../assets/style.css');
</style>