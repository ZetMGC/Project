<template>
    <div id="app">
      <VideoBackground />
      <HeaderMenu />
      <DrupalSupport/>
      <DrupalCompetencies/>
      <DrupalSupp/>
      <expertise-drupal/>
      <tarifFirst/>
      <blockComent/>
      <teamDrupal/>
      <FAQAccordion/>
    </div>
</template>

<script>
import HeaderMenu from "@/components/HeaderMenu.vue";
import VideoBackground from "@/components/VideoBackground.vue";
import DrupalSupport from "@/components/DrupalSupport.vue";
import DrupalCompetencies from "@/components/DrupalCompetencies.vue"
import DrupalSupp from "@/components/DrupalSupp.vue"
import ExpertiseDrupal from "@/components/ExpertiseDrupal.vue";
import tarifFirst from './components/tarifFirst.vue'
import blockComent from './components/blockComent.vue'
import teamDrupal from './components/teamDrupal.vue';
import FAQAccordion from "@/components/FAQAccordion.vue";

export default {
  components: {
    HeaderMenu,
    VideoBackground,
    DrupalSupport,
    DrupalCompetencies,
    DrupalSupp,
    ExpertiseDrupal,
    tarifFirst, 
    blockComent, 
    teamDrupal,
    FAQAccordion
  },
};
</script>

<style>

body {
  margin: 0;
}

</style>