<template>
    <div class="home-page">
        <WorkPhase />
        <MoreQuestion />
        <div class="home-page__connection-btn-wrap">
            <ConnectionBtn />
        </div>
    </div>
</template>

<script>
import ConnectionBtn from "~/components/ConnectionBtn.vue";
import MoreQuestion from '../components/MoreQuestion.vue';
import WorkPhase from '../components/WorkPhase.vue';

export default {
  name: 'IndexPage',

  // layout: 'default',

  //  layout (context) {
  //   return 'default'
  // },

  components: {
    ConnectionBtn,
    MoreQuestion,
    WorkPhase,
   
  },
}
</script>

<style>

.home-page__connection-btn-wrap {
    position: fixed;
    bottom: 85px;
    right: 85px;
}

</style>
