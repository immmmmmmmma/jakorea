<template>
    <div class="reModalWra">
        <div class="reModalTit">
            <h2>모집공고</h2>
            <span>+</span>
        </div>
        <span></span>
        <div class="reListWrap">
            <div class="reTitle">
                <span>모집중</span>
                <p>{{item.title}}</p>
            </div>
            <div class="date">
                <p>{{item.operate}}</p>
            </div>
            <span></span>
        </div>
    </div>
</template>

<script>
export default {
    props:[
        "reData",
    ]
}
</script>

<style lang="scss">

</style>