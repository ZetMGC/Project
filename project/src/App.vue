<template>
    <div id="app">
      <VideoBackground />
      <HeaderMenu />
      <DrupalSupport/>
      <DrupalCompetencies/>
      <DrupalSupp/>
    </div>
</template>

<script>
import HeaderMenu from "@/components/HeaderMenu.vue";
import VideoBackground from "@/components/VideoBackground.vue";
import DrupalSupport from "@/components/DrupalSupport.vue";
import DrupalCompetencies from "@/components/DrupalCompetencies.vue"
import DrupalSupp from "@/components/DrupalSupp.vue"

export default {
  components: {
    HeaderMenu,
    VideoBackground,
    DrupalSupport,
    DrupalCompetencies,
    DrupalSupp
  },
};
</script>

<style>
body {
  margin: 0;
}

</style>
