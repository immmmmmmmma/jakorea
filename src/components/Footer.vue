<template>
    <div class="footer">
        <div class="footerTop">
            <div class="footerInner container">
                <ul class="foInnerWrap">
                    <li><a href="#">이용약관</a></li>
                    <li><a href="#"><b>개인정보처리방침</b></a></li>
                    <li><a href="#">이메일수집거부</a></li>
                    <li><a href="#">오시는길</a></li>
                </ul>
                <botton class="footerBtn">
                    <p>관련 사이트 보기</p>
                    <i class="fa-solid fa-angle-up"></i>
                </botton>
            </div>
        </div>
        <div class="footerMid">
            <div class="footerInner container">
                <ul class="foInnerWrap fm">
                    <li><a href="#">후원하기</a></li>
                    <li><a href="#">온라인 학습관리</a></li>
                    <li><a href="#">기부금영수증</a></li>
                    <li><a href="#">국세청 공시 및 공개 내역</a></li>
                    <li><a href="#">1:1 문의</a></li>
                </ul>
                <div class="footerSns">
                    <p>Follow SNS</p>
                    <ul class="snsIcon">
                        <li><i class="fa-brands fa-facebook"></i></li>
                        <li><i class="fa-brands fa-instagram"></i></li>
                        <li><i class="fa-brands fa-youtube"></i></li>
                    </ul>
                </div>
            </div>

        </div>
        <div class="footerBot container">
            <img :src="`images/footer-logo.svg`" alt="" class="foLogo">
            <p class="foTxt">서울특별시 강서구 양천로 583, B동 1408호&#40;염창동, 우림블루나인비즈니스센터&#41; 사단법인 제이에이코리아 &nbsp;&nbsp;&nbsp;우편번호 : 07547 &nbsp;&nbsp;&nbsp;대표 : 이은형 &nbsp;&nbsp;&nbsp;사업자번호 : 107-82-10367</p>
            <p class="foTxt">대표전화 : 02-783-2367 &nbsp;&nbsp;&nbsp;팩스 : 070-4275-5115 &nbsp;&nbsp;&nbsp;이메일 : jakorea@jakorea.org</p>
            <span>ⓒJA Korea,2022</span>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
    .footerTop{
        width: 100%;
        background: #f5f5f5;
    }
    .footerInner{
     display: flex; 
     padding: 10px 0;
    }
    .foInnerWrap{
        display: flex;
        align-items: center;
        margin-bottom: 0;
        li{
            margin-right: 20px;
            a{
                color: #777;
                font-size: 17px;
                b{
                    color: #285f74;
                }
                &:hover{
                    color: #333;
                }
            }
        }
        &.fm{
            margin-bottom: 40px;
            li>a{
                font-size: 16px;
            }
        }
    }
    .footerBtn{
        display: flex;
        justify-content: flex-start;
        align-items: center;
        margin-left: auto;
        width: 237px;
        height: 42px;
        font-size: 14px;
        padding: 0 19px;
        color: #939393;
        border-radius: 14px;
        background: #fff;
        cursor: pointer;
        i{
            color: #777;
            margin-left: auto;
        }
    }
    .footerSns{
        width: 100px;
        margin-left: auto;
        color: #aaa;
        .snsIcon{
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 20px;
            color: #aaa;
            i{
                cursor: pointer;
                &:hover{
                color: #777;
                }
            }
        }
    }
    .footerBot{
        .foLogo{
            margin-bottom: 40px;
            cursor: pointer;
        }
        .foTxt{
            color: #aaa;
            font-size: 15px;
            margin-bottom: 10px !important;
        }
        span{
            display: block;
            padding: 40px 0;
            font-size: 14px;
            color: #aaa;
        }
    }
</style>