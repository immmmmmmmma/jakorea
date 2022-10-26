<template>
  <div class="container">
    <div class="subscribeWrap">
        <div class="innerBox">
            <h2>JA Korea 뉴스레터 구독하기</h2>
            <div class="inputBox">
                <label>
                    <i class="fa-regular fa-user iuIcon"></i>
                    <input type="text" id="name" placeholder="이름">
                </label>
                <label>
                    <i class="fa-regular fa-envelope ieIcon"></i>
                    <input type="text" id="email" placeholder="이메일 주소">
                </label>
                <button class="subBtn">신청하기</button>
            </div>
            <p><span><i class="fa-regular fa-circle-check"></i></span> 뉴스레터 구독을 위한 이름 및 이메일 주소 수집에 동의합니다.</p>
        </div>
        <img src="images/subscribe-img.png" alt="" class="subsImg">
    </div>
    <div class="upBtn"><i class="fa-solid fa-arrow-up"></i></div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.subscribeWrap{
    position: relative;
    display: flex;
    background: #00a0af;
    background-size: 1000%;
    margin-bottom: 160px;
    background-image: linear-gradient( -45deg,#00a0af,#00c0ca, #008b9c, #28708b,#285f74, #22404d,#285f74,#28708b, #008b9c,#00c0ca,#00a0af) !important;
    border-radius: 20px;
    padding: 44px 56px;
    margin: 0 0 160px 0;
    img{
        width:330px;
        position: absolute;
        right: -4px;
        top: 14px;
    }
}
.innerBox{

    h2{
        font-weight: 700;
        color: #fff;
        margin-bottom: 20px;
    }
    .inputBox{
        margin-bottom: 20px;
    }
    label{
        color: #fff;
        position: relative;
        font-size: 22px;
        .ieIcon,.iuIcon{
            position: absolute;
            left: 40px;
            top: 23px;
        }
    }
    input{
        height: 70px;
        width: 410px;
        margin: 0 20px 0 0;
        padding:  0 70px;
        background: #1ABAC5;
        border-radius: 20px;
        border-style:none;
        &:focus{
            outline: none;
        }
    }
    input::placeholder{color:#fff;}
    .subBtn{
        background: #1ABAC5;
        height: 70px;
        width: 150px;
        border: 1px solid #fff;
        padding: 10px 20px;
        border-radius: 20px;
        color: #fff;
        &:hover{
            color: #1ABAC5;
            background: #fff;
        }
    }
    p{
        color: #fff;
        font-weight: 700;
    }
}
.upBtn{
    right: 40px;
    width: 80px;
    height: 80px;
    color: #fff;
    font-size: 28px;
    font-weight: 300;
    border-radius: 50%;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 3;
    background: #285f74;
    i{
        transition: 0.3s;
    }
    &:hover i{
        transform: translateY(-15px);
    }
}

</style>