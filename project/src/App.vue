<template>
  <TextWork/>
  <CarouselWork/>
</template>

<script>
import TextWork from "@/components/TextWork.vue";
import CarouselWork from "@/components/CarouselWork.vue";


 export default {
   components: {
     TextWork,
     CarouselWork,
   },
   data() {
     return {
        slides: [
            "/images/img1.png"
        ]
     }
   },
 }
</script>

<style>
* {
  margin:0;
  padding:0;
  box-sizing: border-box;
}
</style>
