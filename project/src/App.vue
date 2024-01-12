<template>
    <div id="app">
      <VideoBackground />
      <HeaderMenu />
      <DrupalSupport/>
      <DrupalCompetencies/>
      <DrupalSupp/>
      <expertise-drupal/>
      <tarifFirst/>
      <drupal-tasks/>
      <teamDrupal/>
     
      <lastCases/>
      <blockComent/>
      <FAQAccordion/>
      <working-with-us/>
<<<<<<< HEAD
=======
=======

      <working-with-us/>

>>>>>>> 6f1b35d218abaf0a141e3bb9de1c979ebf633a7b
>>>>>>> 1643f3759b660c4e5e21396f452f00e39068b1ca
      <CarouselWork/>
      <DrupalForm/>
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
import teamDrupal from './components/teamDrupal.vue';
import lastCases from './components/lastCases.vue';
import blockComent from './components/blockComent.vue'
import FAQAccordion from "@/components/FAQAccordion.vue";
import CarouselWork from "@/components/CarouselWork.vue";
import DrupalForm from "@/components/DrupalForm.vue";
import DrupalTasks from "@/components/DrupalTasks.vue";
import WorkingWithUs from "@/components/WorkingWithUs.vue"

export default {
  components: {
    HeaderMenu,
    VideoBackground,
    DrupalSupport,
    DrupalCompetencies,
    DrupalSupp,
    ExpertiseDrupal,

    tarifFirst, 

    teamDrupal,
    
    lastCases,
    blockComent,
    FAQAccordion,
    DrupalForm,
     CarouselWork,
    DrupalTasks,
    WorkingWithUs,
  },
};
</script>

<style>

body {
  margin: 0;
  padding:0;
  box-sizing: border-box;
}

</style>