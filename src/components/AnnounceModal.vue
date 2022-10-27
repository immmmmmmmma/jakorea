<template>
        <div class="anModalTit">
            <h2>결과발표</h2>
            <span><i class="fa-solid fa-plus"></i></span>
        </div>
        <span class="titLine"></span>
    <div class="anModalWrap" v-for="(item,i) in anData" :key="i">
        <div class="anListWrap">
            <div class="anTitle col-11">
                <p>{{item.title}}</p>
            </div>
            <span></span>
        </div>
    </div>
</template>

<script>


export default {
    props:[
        "anData",
    ]
}
</script>

<style lang="scss">
    .anModalTit{
        padding: 0 70px 0 30px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        h2{
            font-size: 35px;
            font-weight: 700;
            line-height: 1;
        }
        span{
            transform: translateY(-10px);
            font-size: 40px;
            transition: 0.3s;
            color: #666;
            &:hover{
                color: #333;
                transform: rotate(180deg);
            }
        }
    }
    .titLine{
        position: absolute;
        // right: 5px;
        content: "";
        width: 600px;
        height: 2px;
        background-color: #333;
    }
    .anModalWrap{
        position: relative;
    }
    .anListWrap{
        overflow: hidden;
        position: absolute;
        display: flex;
        align-items: flex-start;
        padding: 40px 25px;
        border-radius: 26px;
        transition: .3s;
        position: relative;
        border-bottom: 1px solid #e7eced;
        position: relative;
        &:hover{
            box-shadow: 0 0 16px 3px rgb(0 0 0 / 13%);
        }
        .anTitle{
            display: flex;

            p{
                color: #333;
                font-size: 22px;
                font-weight: 700;
                display: block;
                overflow: hidden;
                text-overflow: ellipsis;
                white-space: nowrap;
            }
        }

    }

</style>