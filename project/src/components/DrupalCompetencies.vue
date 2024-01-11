<template>
  <div id="competencies" class="container-fluid">
    <div class="col">
        <div id="head" class="row justify-content-center">
          <div class="col">
            <h2>13 лет совершенствуем компетенции в Drupal поддержке!</h2>
            <div class="description">
              Разрабатываем и оптимизируем модули, расширяем функциональность сайтов, обновляем дизайн
            </div>
          </div>
          <div id="second" class="col"></div>
        </div>
      <div id="compet" class="row">
        <div class="compet-block">
          <img src="../img/competency-1.svg" alt="с1" class="c">
          <p>Добавление информации на сайт, создание новых разделов</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-2.svg" alt="с1" class="c">
          <p>Разработка и оптимизация модулей сайта</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-3.svg" alt="с1" class="c">
          <p>Интеграция с CRM, 1C, платежными системами, любыми веб-сервисами</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-4.svg" alt="с1" class="c">
          <p>Любые доработки фунционала и дизайна</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-5.svg" alt="с1" class="c">
          <p>Аудит и мониторинг безопасности Drupal сайтов</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-6.svg" alt="с1" class="c">
          <p>Миграция, импорт контент и апгрейд Drupal</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-7.svg" alt="с1" class="c">
          <p>Оптимизация и ускорение Drupal-сайтов</p>
        </div>
        <div class="compet-block">
          <img src="../img/competency-8.svg" alt="с1" class="c">
          <p>Веб-маркетинг, консультаци и работы по SEO</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

</script>

<style scoped>
.container {
  padding: 0;
  margin: auto;
}

#competencies {
  background-color: #FFFFFF;
  margin-top: 145px;
  padding-top: 80px;
}

h2 {
  font-family: Montserrat;
  font-size: 42px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin: 0 0 20px;
}

#head {
  margin-left: 230px;
}

.description {
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 22px; /* 137.5% */
}

#compet {
  margin-top: 50px;
  margin-left: 230px;
}

.compet-block {
  width: 260px;
  margin-bottom: 40px;
}

.compet-block p {
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 22px;
  padding-right: 50px;
}

.compet-block::before{
  content: "";
  display: block;
  position: absolute;
  width: 115px;
  height: 70px;
  background: url(../img/icon-drupal.svg) no-repeat center;
  background-size: contain;
}

.compet-block img {
  margin-bottom: 30px;
}

@media (min-width: 860px) and (max-width: 925px) {
  #compet {
    margin-left: 60px;
  }
}

@media (min-width: 600px) and (max-width: 860px) {
  #compet {
    margin-left: 120px;
  }

  #head {
    margin-left: 10%;
  }

  #second {
    display: none;
  }

  .compet-block {
    width: 200px;
  }

  .compet-block p {
    padding: 0;
  }
}

@media (min-width: 1000px) and (max-width: 1480px) {
  #compet {
    margin-left: 120px;
  }

  #head {
    margin-left: 120px;
  }
}

@media (min-width: 200px) and (max-width: 600px) {
  #compet {
    margin-left: 10px;
  }

  #second {
    display: none;
  }

  #head {
    margin-left: 5%;
  }

  #head h2 {
    font-size: 30px;
  }

  .compet-block {
    width: 200px;
  }

  .compet-block p {
    padding: 0;
  }
}

@media screen and (max-width: 430px) {
  .compet-block {
    width: 135px;
    padding-left: 0;
  }

  #compet {
    justify-content: center;
  }

  #head h2 {
    font-size: 26px;
  }

  #competencies {
    padding-left: 0;
  }
}

@media screen and (max-width: 1200px) {
  #competencies {
    margin-top: 0;
  }
}
</style>