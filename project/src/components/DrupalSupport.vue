<template>
  <div id="support">
    <div class="row justify-content-center">
      <div id="MainDrupal">
        <h1>Поддержка сайтов на Drupal</h1>
        <p class="lead">Сопровождение и поддержка сайтов на CMS Drupal любых версий и запущенности</p>
        <a id="tariffBtn" class="btn btn-outline-primary" type="button" href="#">ТАРИФЫ</a>
      </div>
      <div id="merits">
        <div class="row">
          <MeritItem v-for="merit in merits" :merit="merit" :key="merit.id"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MeritItem from "@/components/MeritItem.vue";
export default {
  components: {
    MeritItem,
  },
  data() {
    return {
      merits: [
        {id: 1, title: '#1', body: 'Drupal разработчик в России по версии Рейтинга Рунета'},
        {id: 2, title: '3+', body: 'средний опыт специальистов более 3 лет'},
        {id: 3, title: '14', body: 'лет опыта в сфере Drupal'},
        {id: 4, title: '50+', body: 'модулей и тем в формате DrupalGive'},
        {id: 5, title: '90 000+', body: 'часов поддержки сайтов на Drupal'},
        {id: 6, title: '300+', body: 'Проектов на поддержке'},
      ],
    }
  },
}
</script>

<style scoped>

h1, p {
  color: #FFFFFF;
}

a {
  font-size: 12px;
  padding: 20px 100px;
  color: white;
  --bs-btn-hover-bg: #F14D34;
  --bs-btn-hover-border-color: #F14D34;
  --bs-btn-border-color: #F14D34;
  --bs-btn-active-bg: #F14D34;
  --bs-border-width: 3px;
}

#support {
  width: 100%;
}

#MainDrupal a {
  margin-top: 50px;
  margin-left: 10%;
}

#MainDrupal {
  margin-top: 50px;
}

@media screen and (max-width: 1890px) {
  #merits {
    width: 40%;
  }
}

@media screen and (min-width: 690px) {

  #support {
    font-family: Montserrat;
    margin-top: 130px;
  }

  #MainDrupal {
    width: 28%;
  }

  p {
    font-size: 18px;
    font-style: normal;
    font-weight: 300;
    line-height: 28px;
    margin-top: 15px;
    opacity: 0.8;
  }

  h1 {
    font-style: normal;
    font-weight: 700;
    line-height: 60px;
    font-size: 52px;
  }

  #merits {
    margin-left: 50px;
    width: 30%;
  }

  h3 {
    font-size: 48px;
  }

  #tariffBtn {
    margin-top: 55px;
  }
}

@media (min-width: 1410px) and (max-width: 1890px) {
  #merits {
    width: 40%;
  }
}

@media (min-width: 1200px) and (max-width: 1410px) {
  #merits {
    width: 50%;
  }
}

@media screen and (max-width: 1200px) {

  #MainDrupal {
    width: 80%;
  }

  #MainDrupal h1 {
    text-align: center;
  }

  #MainDrupal p {
    text-align: center;
  }

  #merits {
    width: 70%;
  }
}

@media (min-width: 1000px) and (max-width: 1200px) {
  #MainDrupal a {
    margin-left: 35%;
  }

  #support {
    margin-top: 0px;
  }

  #merits {
    width: 60%;
    margin-left: 10%;
  }
}

@media (min-width: 690px) and (max-width: 1000px) {
  #MainDrupal a {
    margin-left: 30%;
  }

  #merits {
    width: 75%;
    margin-left: 20%;
  }

  #support {
    margin-top: 0px;
  }
}

@media (min-width: 400px) and (max-width: 690px) {
  #MainDrupal a {
    margin-left: 20%;
  }

  #merits {
    width: 100%;
    margin-left: 25%;
  }
}

@media (min-width: 540px) and (max-width: 590px) {
  #merits {
    width: 70%;
    margin-left: 15%;
  }
}

@media (min-width: 300px) and (max-width: 540px) {
  #merits {
    width: 98%;
    margin-left: 20%;
  }
}

@media screen and (max-width: 300px) {
  #MainDrupal a {
    margin-left: 0px;
    padding: 15px 80px;
  }

  #merits {
    width: 98%;
    margin-left: 10%;
  }
}
</style>