<template>
  <div class="container-fluid" style="margin-top: 100px; margin-bottom: -120px">
    <div class="row justify-content-center">
      <div class="col-lg-11 col-xs-12 col-sm-10 col-md-12">
        <h2 class="text-center">
          Поддержка <br/> от Drupal-coder
        </h2>
        <div id="support" class="row justify-content-center">
          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">01.</div>
                <div class="title">Постановка задачи по Email</div>
              </div>
              <div class="body">
                Удобная и привычная модель постановки задач, при которой задачи фиксируются и никогда не теряются.
              </div>
              <div class="icon">
                <img src="@/img/support1.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">02.</div>
                <div class="title">Система Helpdesk – отчетность, прозрачность</div>
              </div>
              <div class="body">
                Возможность посмотреть все заявки в работе и отработанные часы в личном кабинете через браузер.
              </div>
              <div class="icon">
                <img src="@/img/support2.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">03.</div>
                <div class="title">Расширенная техническая поддержка</div>
              </div>
              <div class="body">
                Возможность организации расширенной техподдержки с 6:00 до 22:00 без выходных.
              </div>
              <div class="icon">
                <img src="@/img/support3.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">04.</div>
                <div class="title">Персональный менеджер проекта</div>
              </div>
              <div class="body">
                Ваш менеджер проекта всегда в курсе текущего состояния проекта и в любой момент готов ответить на любые вопросы.
              </div>
              <div class="icon">
                <img src="@/img/support4.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">05.</div>
                <div class="title">Удобные способы оплаты</div>
              </div>
              <div class="body">
                Безналичный расчет по договору или электронные деньги: WebMoney, Яндекс.Деньги, Paypal.
              </div>
              <div class="icon">
                <img src="@/img/support5.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">06.</div>
                <div class="title">Работаем с SLA и NDA</div>
              </div>
              <div class="body">
                Работа в рамках соглашений о конфиденциальности и об уровне качества работ.
              </div>
              <div class="icon">
                <img src="@/img/support6.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">07.</div>
                <div class="title">Штатные специалисты</div>
              </div>
              <div class="body">
                Надежные штатные специалисты, никаких фрилансеров.
              </div>
              <div class="icon">
                <img src="@/img/support7.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-3 col-xs-12 support-block">
            <div class="content">
              <div class="header">
                <div class="number">08.</div>
                <div class="title">Удобные каналы связи</div>
              </div>
              <div class="body">
                Консультации по телефону, скайпу, в месенджерах.
              </div>
              <div class="icon">
                <img src="@/img/support8.svg" alt="Постановка задачи по Email" class="img-responsive" height="84" width="84">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>

</template>

<script>

</script>

<style scoped>

* {
  font-family: Montserrat;
}

h2 {
  font-size: 42px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-bottom: 56px;
}

.support-block {
  margin-bottom: 5px;
  margin-right: 5px;
}

.content {
  background: #fff;
  border-radius: 5px;
  box-shadow: 0 20px 40px rgba(5,12,51,.15);
  margin-left: -12px;
  margin-right: -12px;
  height: 100%;
  position: relative;
  padding: 25px 25px 45px;
  min-height: 292px;
}

.number {
  font-weight: 700;
  font-size: 12px;
  color: #828a9b;
  margin-bottom: 20px;
}

.title {
  font-weight: 700;
  font-size: 18px;
  color: #050c33;
  line-height: 1.22;
  margin-bottom: 15px;
}

.body {
  position: relative;
  z-index: 10;
  font-weight: 500;
  font-size: 16px;
  color: #4e5a73;
  line-height: 1.37;
}

.icon {
  position: absolute;
  right: 0;
  bottom: 0;
  z-index: 5;
}

@media screen and (min-width: 1000px) {
  .support-block {
    max-width: 280px;
  }
}

</style>