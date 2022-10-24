<template>
  <div class="slideWrap">
    <div class="container menuWrap">
        <div class="row tabMenu">
        <h1>JA 기관소식</h1>
          <div class="col tab" @click="tab=1" :class="{active:tab==1}">
            공지사항<span></span>
          </div>
          <div class="col tab" @click="tab=2" :class="{active:tab==2}">
            스토리<span></span>
          </div>
          <div class="col tab" @click="tab=3" :class="{active:tab==3}">
            언론보도<span></span>
          </div>
        </div>
        <TabSlide
            :noData="noData"
            :stData="stData"
            :neData="neData"
            :tab="tab">
        </TabSlide>
    </div>
  </div>
</template>

<script>
import TabSlide from "../components/TabSlide.vue";

export default {
  components: { TabSlide },
  props: [
    "noData",
    "stData",
    "neData"
    ],
  data() {
    return {
      tab: 1,
    };
  },
};
</script>

<style lang="scss" scoped>
.container{
    display: flex;
    flex-direction: column;
    h1 {
      width: 300px;
      font-weight: 700;
    }
}

.tabMenu {
    width: 100%;
    display: flex;
    font-size: 1.3em;
    div {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    position: relative;
    span {
        width: 70%;
        height: 5px;
        position: absolute;
        bottom: 10%;
        background: #365a66;
        display: none;
    }
    &.active {
        span {
        display: block;
        }
    }
  }
}
  .notice-slide-tap {
    height: 100%;
  }
</style>