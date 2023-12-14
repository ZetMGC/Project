<template>
    <div id="app">
      <VideoBackground />
      <HeaderMenu />
      <DrupalSupport/>
    </div>
</template>

<script>
import HeaderMenu from "@/components/HeaderMenu.vue";
import VideoBackground from "@/components/VideoBackground.vue";
import DrupalSupport from "@/components/DrupalSupport.vue";

export default {
  components: {
    HeaderMenu, 
    VideoBackground,
    DrupalSupport,
  },
};
</script>

<style>
body {
  margin: 0;
}

#app {
  height: 1080px;
  overflow-x: hidden;
}

</style>
