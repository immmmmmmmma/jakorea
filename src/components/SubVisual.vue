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
            <button class="btn">
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
    text-align: left;
    p{
        font-size: 38px;
        font-weight: 200;
        text-align: left;
        color: #fff;
        display: inline;
        padding: 8px 12px 2px;
        background-repeat: no-repeat;
        background-size: 0% 92%;
        transition: background-size 1.5s 0s;
        background-position: left bottom;
        background-image: linear-gradient(to right, #00a0af, #00a0af);
        top: 50px;
        opacity: 0;
        position: relative;
        &.on{
            background-size: 100% 92%;
            opacity: 1;
            transition: background-size 1.5s 2s, top 1.2s 0s, opacity 1.7s 0s;
            top: 0;
            opacity: 1;
        }
    }
    ul{
        text-align: left;
        height: 98px;
        margin-top: 20px;
    }
}
.typing ul li{
    display: block;
    font-family: "NanumSquareEB";
    color: #fff;
    font-size: 75px;
    text-align: left;
    line-height: 1.3;
    &.on{
        display: inline-block;
        animation-name: cursor;
        animation-duration: 0.3s;
        animation-iteration-count: infinite;
    }
}
@keyframes cursor {
    to{width: 0;}
    from{width: 100%;}
}

</style>