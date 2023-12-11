<template>
    <div id="app">
      <VideoBackground />
      <HeaderMenu />
    </div>
</template>

<script>
import HeaderMenu from "@/components/HeaderMenu.vue";
import VideoBackground from "@/components/VideoBackground.vue";

export default {
  components: {
    HeaderMenu, 
    VideoBackground,
  },
};
</script>

<style>
body {
  margin: 0;
}

#app {
  height: 1080px;
}

</style>
