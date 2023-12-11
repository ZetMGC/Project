<template>
    <div class="video-container">
      <video autoplay muted loop class="video-background" >
        <source :src="videoSource" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        videoSource: require('@/img/video.mp4')
      };
    }
  };
  </script>
  
  <style scoped>
  .video-container {
    position: relative;
  }
  
  .video-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    object-fit: cover;
  }
  
  .video-background video {
    width: 100%;
    height: auto;
  }
  
  </style>
  