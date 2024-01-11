<template>
  <TextWork/>
  <CarouselWork/>
  <DrupalForm/>
</template>

<script>
import TextWork from "@/components/TextWork.vue";
import CarouselWork from "@/components/CarouselWork.vue";
import DrupalForm from "@/components/DrupalForm.vue";

 export default {
   components: {
     DrupalForm,
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
