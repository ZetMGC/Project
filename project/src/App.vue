<template>
    <div id="app">
      <VideoBackground />
      <HeaderMenu />
      <DrupalSupport/>
      <DrupalCompetencies/>
    </div>
</template>

<script>
import HeaderMenu from "@/components/HeaderMenu.vue";
import VideoBackground from "@/components/VideoBackground.vue";
import DrupalSupport from "@/components/DrupalSupport.vue";
import DrupalCompetencies from "@/components/DrupalCompetencies.vue"


export default {
  components: {
    HeaderMenu,
    VideoBackground,
    DrupalSupport,
    DrupalCompetencies,
  },
};
</script>

<style>
body {
  margin: 0;
}

</style>
