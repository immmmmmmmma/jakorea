<template>
  <MainHeader></MainHeader>
  <MainVisual :mainsData="msData"></MainVisual>
  <icon-banner :ibData="ibData"></icon-banner>
  <EduSlide :epData="epData"></EduSlide>
  <CountBanner></CountBanner>
  <NoticeTab    
    :noData="noData"
    :stData="stData"
    :neData="neData">
  </NoticeTab>
  <NewsModal></NewsModal>
  <SubVisual></SubVisual>
  <SupportSlide></SupportSlide>
  <SubcribeBanner></SubcribeBanner>
  <Footer></Footer>


</template>

<script>
import MainHeader from './components/MainHeader.vue'
import MainVisual from './components/MainVisual.vue'
import IconBanner from './components/IconBanner.vue'
import EduSlide from './components/EduSlide.vue'
import CountBanner from './components/CountBanner.vue'
import NoticeTab from './components/NoticeTab.vue'
import NewsModal from './components/NewsModal.vue'
import SubVisual from './components/SubVisual.vue'
import SupportSlide from './components/SupportSlide.vue'
import SubcribeBanner from './components/SubcribeBanner.vue'
import Footer from './components/Footer.vue'

import msData from '@/data/01mainSlide.js'
import ibData from '@/data/02iconBanner.js'
import epData from '@/data/03eduProgram.js'
import noData from '@/data/04notice.js'
import stData from '@/data/05notice.js'
import neData from '@/data/06new.js'
import reData from '@/data/07notice.js'
import anData from '@/data/08result.js'
import suData from '@/data/09support.js'

export default {
  name: 'App',
  components: {
    MainHeader,
    MainVisual,
    IconBanner,
    EduSlide,
    CountBanner,
    NoticeTab,
    NewsModal,
    SubVisual,
    SupportSlide,
    SubcribeBanner,
    Footer,
  },
  data(){
    return{
      msData:msData,
      ibData:ibData,
      epDaTa:epData,
      noData:noData,
      stData:stData,
      neData:neData,
      reData:reData,
      anData:anData,
      suData:suData

    }
  }
}
</script>

<style lang="scss">
@import url(./assets/style.css);
</style>
