<template>
<div class="wrap">
    <img :src="`./images/02iconBanner/${item.src}`" alt="">
    <h4 v-html="item.title"></h4>
    <p v-html="item.subtitle"></p>
    mjgkhlk
</div>
</template>

<script>
export default {
    props:["ibData"],
}
</script>

<style>

</style>