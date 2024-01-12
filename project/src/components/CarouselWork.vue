<template>
  <div class="container-fluid">
    <div class="sliders-container row ">
    <swiper class="slider"
        :modules="modules"
            :breakpoints="{ 600:{ slidesPerView:2 }, 900:{slidesPerView: 3}, 1500:{ slidesPerView:5, } }"
        :space-between="20"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
            :autoplay="autoplay[0]"
    >
      <swiper-slide class="img-slider"><img src="../../public/images/img1.png " ></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img4.jpg"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img2.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img3.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img5.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img7.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img6.png"></swiper-slide>
    </swiper>
    <swiper class="slider2"
            :modules="modules"
            :breakpoints="{ 600:{ slidesPerView:2 }, 900:{slidesPerView: 3}, 1530:{ slidesPerView:5 } }"
            :space-between="20"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
            :autoplay="autoplay[1]"
    >
      <swiper-slide class="img-slider"><img src="../../public/images/img8.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img9.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img10.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img11.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img12.jpg"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img13.png"></swiper-slide>
      <swiper-slide class="img-slider"><img src="../../public/images/img14.png"></swiper-slide>
    </swiper>
    </div>
  </div>
</template>
<script>
// import Swiper core and required modules
import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from 'swiper/modules';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';


// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/autoplay';

// Import Swiper styles
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {

    const onSwiper = (swiper) => {
      console.log(swiper);
      swiper.autoplay.start();
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    const modules = [Navigation, Pagination, Scrollbar, A11y, Autoplay];
    const autoplay =  [
      { delay: 5000, disableOnInteraction: false},
      { delay: 7000, disableOnInteraction: false},
    ];
    return {
      onSwiper,
      onSlideChange,
      modules,
      autoplay,
    };
  },
};
</script>
<style scoped>

.slider {
  height: 125px;
}
.slider2 {
  margin-top:20px;
  height: 125px;
}
.img-slider {
  positon: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #afa7a7;
  border-radius: 7px;
  width: 291px;
  height: 155px;
}

.img-slider {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.sliders-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.container-fluid {
  max-width: 95%;
}

</style>