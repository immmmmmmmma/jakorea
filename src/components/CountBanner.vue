<template>
  <div class="countBannerWrap">
    <div><img :src="`./images/main-number-1.jpg`" alt="" class="col-12 col-md-5"></div>
    <ul class="count col-12 col-md-7">
        <li>
            <span class="countBar"></span>+200
            <p><b>지역 네트워크</b>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
        </li>
        <li>
            <span class="countBar"></span>+1,000
            <p><b>학교 및 기관</b>전국 1,000여개 학교 및 기관, 단체와 협업하여 교육을 진행합니다.</p>
        </li>
        <li>
            <span class="countBar"></span>+3,000
            <p><b>교육 진행자</b>3,000여명의 전문 지식을 갖춘 봉사자와 교사, 강사가 함께 교육을 진행하고 있습니다.</p>
        </li>
        <li>
            <span class="countBar"></span>+90,000
            <p><b>교육 수혜자</b>전국 90,000여명의 청소년들이 교육 프로그램에 참여합니다.</p>
        </li>
    </ul>
  </div>

</template>


<script>
export default {

}
</script>

<style lang="scss">
.countBannerWrap{
    background: linear-gradient(135deg,  #e0aff9 0%,#01a1ad 68%);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
    display: flex;
    justify-content: center;
    padding: 100px 100px;
    div{
        // overflow: hidden;

        img{
            border-radius: 30px;
            width: 400px;
        }
    }
    
}
@keyframes gradient {
     0% { background-position: 0% 50%; } 
     50% { background-position: 100% 50%; } 
     100% { background-position: 0% 50%; } 
     }
.countBar{
    display: block;
    content: "";
    width: 705px;
    height: 10px;
    border-radius: 5px;
    background: #00a0af;
}


</style>