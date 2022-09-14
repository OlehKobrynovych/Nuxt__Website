<template>
    <div class="home-page">
        <OurServices />
        <PortfolioSlider />
        <WorkPhase />
        <MoreQuestion />
        <ContactForm />
        <div class="home-page__connection-btn-wrap">
            <ConnectionBtn />
        </div>
    </div>
</template>

<script>
import ConnectionBtn from "~/components/ConnectionBtn.vue";
import MoreQuestion from '../components/MoreQuestion.vue';
import WorkPhase from '../components/WorkPhase.vue';
import ContactForm from '../components/ContactForm.vue';
import PortfolioSlider from '../components/PortfolioSlider.vue';
import OurServices from '../components/OurServices.vue';

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
    ContactForm,
    PortfolioSlider,
    OurServices,
   
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
