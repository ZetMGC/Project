<template>
  <div id="support">
    <div class="row justify-content-center">
      <div class="col">
        <div class="row justify-content-center">
          <div class="col-4">
            <h1>Поддержка сайтов на Drupal</h1>
            <p class="lead">Сопровождение и поддержка сайтов на CMS Drupal любых версий и запущенности</p>
            <a id="tariffBtn" class="btn btn-outline-primary" type="button" href="#">ТАРИФЫ</a>
          </div>
          <div id="merits" class="col-5">
            <div class="row">
              <MeritItem v-for="merit in merits" :merit="merit" :key="merit.id"/>
            </div>

          </div>
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
#support {
  font-family: Montserrat;
  margin-top: 130px;
}

h1, p {
  color: #FFFFFF;
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

#merits {
  margin-left: 50px;
}

h3 {
  font-size: 48px;
}

#tariffBtn {
  margin-top: 55px;
}
</style>