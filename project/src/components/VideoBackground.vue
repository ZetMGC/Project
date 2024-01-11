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
    z-index: -1000;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 900px;
    background-color: rgba(0, 0, 0, 0.5); /* Пример: затемнение с прозрачностью 0.5 */
  }

  .video-background {
    position: absolute;
    top: 0;
    left: 0;
    object-fit: cover;
    width: 100%;
    height: 700px;
  }

  .video-container::after {
    content: "";
    display: block;
    width: 100%;
    height: 700px;
    background-color: black;
    opacity: 0.7;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 100;
  }

  @media screen and (min-width: 1200px) {
    .video-background {
      position: absolute;
      top: 0;
      left: 0;
      width:100%;
      object-fit: cover;
    }
  }

  @media screen and (max-width: 530px) {
    .video-background {
      height: 800px;
    }

    .video-container::after {
      height: 800px;
    }
  }

  </style>
  