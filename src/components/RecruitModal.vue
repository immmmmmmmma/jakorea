<template>
        <div class="reModalTit">
            <h2>모집공고</h2>
            <span><i class="fa-solid fa-plus"></i></span>
        </div>
        <span class="titLine"></span>
    <div class="reModalWrap" v-for="(item,i) in reData" :key="i">
        <div class="reListWrap">
            <div class="reTitle col-11">
                <span>모집중</span>
                <p>{{item.title}}</p>
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
    .reModalTit{
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
        content: "";
        width: 100%;
        height: 2px;
        background: #333;
    }
    .reModalWrap{
        position: relative;
    }
    .reListWrap{
        overflow: hidden;
        position: absolute;
        display: flex;
        align-items: flex-start;
        padding: 37px 25px;
        border-radius: 26px;
        transition: .3s;
        position: relative;
        border-bottom: 1px solid #e7eced;
        position: relative;
        &:hover{
            box-shadow: 0 0 16px 3px rgb(0 0 0 / 13%);
        }
        .reTitle{
            display: flex;
            span{
                // width: 35px;
                background: #285f74;
                padding: 8px 10px;
                color: #fff;
                border-radius: 20px;
                margin-right: 15px;
                position: relative;
                top: -4px;
                flex-shrink: 0;
            }
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