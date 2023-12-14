<template>
  <div class="merit">
    <div class="row"><h3 :id="merit.id">{{ merit.title }}</h3><img v-if="merit.id == '1'" src="@/img/cup.png" alt=""></div>
    <div><p>{{ merit.body }}</p></div>
  </div>
</template>

<script>
export default {

  props: {
    merit: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>



h3, p {
  color: white;
}

h3 {
  margin-top: 7px;
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

p {
  font-size: 12px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  opacity: 0.8;
}

[id="1"] {
  font-size: 48px;
  margin-top: -22px;
  width: fit-content;
  padding-right: 0px;
}

img {
  margin-top: -28px;
  pading: 0px;
  width: 50%;
  height: 70%;
}

.merit {
  width: 166px;
  margin-right: 25px;
  margin-bottom: 50px;
  margin-top: 50px;
  height: 90px;
  border-left: 3px solid #EF4D35;
}
</style>