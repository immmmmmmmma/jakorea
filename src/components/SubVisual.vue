<template>
    <div class="secVideo">
        <div class="mainVideo">
            <video muted="" loop="" autoplay="" playsinline="" preload="metadata" poster="" id="mainVdo">
                <source src="../../public/images/main-home.mp4" type="video/mp4">
            </video>
        </div>
        <div class="innerText02">
            <div class="typing">
                <p>우리 청소년들이 미래의 인재로 성장하도록</p>
                <h2>JA KOREA가 함께합니다.</h2>
            </div>
            <button class="btn tp">
                <span>
                    자세히 보기<i class="fa-solid fa-arrow-right-long"></i>
                </span>
                <div class="gradient"></div>
            </button>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">

.secVideo{
        margin-bottom: 220px;
        position: relative;
    }
.innerText02{
    top: 0;
    left: 40px;
    position: absolute;
    height: 100%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: flex-start;
    .btn.tp{
        margin-left: 200px;
    }
}
.mainVideo {
    position: relative;
    text-align: center;
    height: calc(100vh);
    height: calc(var(--vh, 1vh) * 100);
    overflow: hidden;
}
#mainVdo{
    width: 100%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.typing{
    margin-left: 200px;
    text-align: left;
    p{
        font-size: 38px;
        font-weight: 200;
        text-align: left;
        color: #fff;
        display: inline;
        padding: 8px 12px 2px;
        background-repeat: no-repeat;
        background-size: 100% 92%;
        background-position: left bottom;
        background-image: linear-gradient(to right, #00a0af, #00a0af);
    }
    h2{
        font-size: 75px;
        color: #fff;
        font-weight: 700;
    }
}
.btn.tp{
    background: #285F74;
    span{
        color: #fff;
    }
    &:hover{
        background: #285F74;
    }
}

</style>