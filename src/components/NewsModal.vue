<template>
    <div class="newWrap container">
        <div class="recruitView col-md-6 col-12">
            <recruit-modal :reData="reData"></recruit-modal>
        </div>
        <div class="announceView col-md-6 col-12">
            <announce-modal :anData="anData"></announce-modal>
        </div>
    </div>
</template>

<script>
import RecruitModal from './RecruitModal.vue'
import AnnounceModal from './AnnounceModal.vue'

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
        margin-bottom: 180px;
    }
    .recruitView{
        margin-right: 50px;
    }
    .announceView{
        margin-left: 50px;
    }

</style>