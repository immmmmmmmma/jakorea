<template>
<div class="modal">
        <slot name="header">
        </slot>
        <slot name="body">
            <div class="modalHead">
                <h3>{{item.title}}</h3>
                <span></span>
            </div>
            <div class="modalInfo">
                <div class="img">
                    {{item.s_src}}
                </div>
                <ul class="info">
                    <li>
                        <h4>대상</h4>
                        <span>{{item.target}}</span>
                    </li>
                    <li>
                        <h4>모집</h4>
                        <span>{{item.target}}</span>
                    </li>
                    <li>
                        <h4>발표</h4>
                        <span>{{item.target}}</span>
                    </li>
                    <li>
                        <h4>운영</h4>
                        <span>{{item.target}}</span>
                    </li>
                    <li>
                        <h4>후원사</h4>
                        <span>{{item.target}}</span>
                    </li>
                    <button>참가 신청하기</button>
                </ul>
            </div>
            <div class="modalCon">
                <img :src="`./images/07notice/${item.b_src}`" alt="">
                <p v-html="item.subcontent"></p>
            </div>
        </slot>
        <button class="closeBtn"><i class="fa-solid fa-xmark"></i></button>
</div>
</template>

<script>
export default {

}
</script>

<style>
    .modal{
        width: 700px;
        height: 900px;
        background: #fff;
        position: fixed;
        left: 50%;
        top: 10%;
        margin-left: -150px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column ;
        gap: 20px;
        border-radius: 20px;
        box-shadow: 0 0 10px rgb(0, 0, 0, 0.3);
        overflow: hidden;
        }
</style>