<template>
<div id="expertise" class="container-fluid" style="background-color: #040613">
  <div class="row justify-content-center">
    <div class="col-lg-6 col-xs-12 col-sm-12 col-md-12 order-2 order-xs-2 order-sm-2 order-lg-1" style="margin: 0; padding: 0">
      <div class="expertise-img">
        <img src="@/img/laptop.png" alt="Laptop">
      </div>
    </div>
    <div id="content" class="col order-1 order-xs-1 order-sm-1 order-lg-2">
      <h2 class="title">Экспертиза в Drupal, <br> опыт 18 лет!</h2>
      <div class="row">
        <div class="col-7 col-lg-6 expertise">Только системный подход – контроль версий, резервирование и тестирование!</div>
        <div class="col-7 col-lg-6 expertise">Только Drupal сайты, не берем на поддержку сайты на других CMS!</div>
        <div class="col-7 col-lg-6 expertise">Участвуем в разработке ядра Drupal и модулей на Drupal.org, разрабатываем свои модули Drupal</div>
        <div class="col-7 col-lg-6 expertise">Поддерживаем сайты на Drupal 5, 6, 7 и 8</div>
      </div>
    </div>
  </div>
</div>
</template>

<script setup>

</script>

<style scoped>
* {
  font-family: Montserrat;
}

h2 {
  font-weight: 700;
  font-size: 42px;
  margin-bottom: 65px;
  color: white;
}

.expertise-img img {
  width: 100%;
  height: auto;
  transform: translateY(10%);
}

#content {
  margin-top: 150px;
}

#expertise {
  padding-top: 200px;
}

.expertise {
  height: 106px;
  color: white;
  border-left: 3px solid #f14d34;
  padding-left: 15px;
  padding-top: 5px;
  padding-bottom: 10px;
  min-height: 88px;
  font-weight: 500;
  font-size: 16px;
  color: rgba(256,256,256,.7);
  width: 260px;
  max-width: 100%;
  margin-bottom: 40px;
}

@media screen and (max-width: 768px) {
  .expertise {
    margin-left: 10px;
  }
}

@media screen and (max-width: 450px) {
  h2 {
    font-size: 30px;
  }
}
</style>