<template>
    <div class="newWrap container">
        <recruit-modal :reData="reData">A</recruit-modal>
        <announce-modal :anData="anData">B</announce-modal>
    </div>
</template>

<script>
import AnnounceModal from './AnnounceModal.vue'
import RecruitModal from './RecruitModal.vue'

export default {
  components: {
    RecruitModal,
    AnnounceModal,
    },
    props:[
        "reData",
        "anData",
    ],
}
</script>

<style lang="scss">
    .newWrap{
        display: flex;
    }
</style>