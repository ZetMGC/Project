<template>
  <div class="container" style="margin-top: 40px">
    <div class="col">
      <h2 class="text-center">Наши разработчики <br> выполняют быстро любые задачи</h2>
    </div>

    <div class="row justify-content-center">
      <div class="col-xs-10 col-sm-10 col-md-6 col-7">
        <div class="row justify-content-center">
          <div class="col competency">
            <div class="icon">
              <img src="@/img/competency-20.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
            </div>
            <div class="handler">от 1ч</div>
            <div class="body">Настройка события GA в интернет магазине</div>
          </div>

          <div class="col competency">
            <div class="icon">
              <img src="@/img/competency-21.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
            </div>
            <div class="handler">от 1ч</div>
            <div class="body">Настройка события GA в интернет магазине</div>
          </div>

          <div class="col competency">
            <div class="icon">
              <img src="@/img/competency-22.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
            </div>
            <div class="handler">от 1ч</div>
            <div class="body">Настройка события GA в интернет магазине</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
h2 {
  font-size: 42px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-bottom: 56px;
}

.handler {
  font-size: 30px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.body {
  font-weight: 500;
  font-size: 16px;
  color: #4e5a73;
  line-height: 1.37;
}

.icon::before{
  content: "";
  display: block;
  position: absolute;
  width: 115px;
  height: 70px;
  background: url(../img/icon-drupal.svg) no-repeat center;
  background-size: contain;
}

.competency {
  padding-right: 20px;
  margin-bottom: 40px;
}

@media screen and (max-width: 900px) {
  h2 {
    font-size: 30px;
  }
}
</style>