<template>
  <div class="cont row">
    <div class="text col">
      <div class="header">
        Оставить заявку на <br>
        поддержку сайта <br>
      </div>
      <div class="mainText">
        Срочно нужна поддержка сайта? Ваша команда не успевает <br>
          справиться самостоятельно или предыдущий подрядчик не <br>
        справился с работой? Тогда вам точно к нам! Просто оставьте <br>
        заявку и наш менеджер с вами свяжется!
      </div>
      <div class="tel"><img src="../../public/images/phone-line%20(2).png">8 800 222-26-73</div>
      <div class="e-mail"><img src="../../public/images/mail.png">info@drupal-coder.ru</div>

    </div>
    <div class="formDrupal col">
      <form>
        <input type="text" class="form-control" name="fullName" placeholder="Ваше имя" >
        <input type="tel" class="form-control" name="phone" placeholder="Телефон" pattern="[0-9]+" required >
        <input type="email" class="form-control" name="e-mail" placeholder="E-mail" >
        <textarea id="message" class="form-control" rows="4" placeholder="Ваш комментарий"></textarea>
        <div class="checkboxForm">
          <div class="form-check">
            <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
            <label class="form-check-label" for="flexCheckDefault">
              <p>Отправляя заявку, я даю согласие <a href="https://drupal-coder.ru/privacy-policy" target="_blank"> на обработку своих персональных данных</a> </p>
            </label>
          </div>
        </div>
        <button type="button" class="btn btn-danger">Свяжитесь с нами</button>
      </form>
    </div>
  </div>
  <div class="footer row">

  </div>
</template>

<script setup>

</script>

<style scoped>
* {
  background-color: #040613;
  font-family: Montserrat;
}

.text {
  margin-top: 40px;
  margin-left: 130px;
}

.container-fluid {
  margin-top: 100px;
  padding-top: 10px;
}

.header {
  color: #FFF;

  /* titles/h2 */
  font-family: Montserrat;
  font-weight: 700;
  font-size: 42px;
  line-height: 1.215;
  margin-bottom: 20px;
}

.mainText {
  color: #FFF;

  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 22px; /* 157.143% */
  opacity: 0.7;
}

.tel {
  color: #FFFFFF;
  font-family: Montserrat;
  font-size: 22px;
  font-style: normal;
  font-weight: 700;
  line-height: 150%; /* 48px */
  margin-top: 142px;
}

.tel img {
  padding-right: 10px;
  padding-bottom: 5px;
}
.e-mail {
  color: #FFFFFF;
  font-family: Montserrat;
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 150%; /* 27px */
  text-decoration-line: underline;
}
.e-mail img {
  padding-right: 10px;
  padding-bottom: 5px;
}
.formDrupal > form {
  padding: 40px;
}
.formDrupal > form > .form-control{
  width: 480px;
  height: 67px;
  background-color: #040613; /* Цвет фона */
  color: #FFF; /* Цвет текста */
  border-color: #FFFFFF; /* Цвет границы инпута */
}

.formDrupal > form > .form-control::placeholder {
  color: white;
}

.formDrupal > form > .form-control:focus {
  outline: none;
  border-color: #EF4D32; /* Оранжевый цвет границы при фокусировке */

}


.form-control {
  display: block;
  width: 100%;
  height: 36px;
  padding: 6px 12px;
  margin-top: 20px;
  font-size: 16px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075);
  -webkit-transition: border-color ease-in-out .15s,box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s,box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s,box-shadow ease-in-out .15s;
}

#message {
  height:120px;
}

.checkboxForm {
  margin-top: 10px;
  display: flex;
  flex-direction: row;
}

.form-check-input {
  background-color: transparent; /* Прозрачный фон */
  border: 2px solid #EF4D32; /* Оранжевая окантовка */
}

.form-check-input:checked {
  background-color: #EF4D32; /* Оранжевый фон при выборе */
  border-color: #EF4D32; /* Оранжевая окантовка при выборе */
}
.form-check-label p {
  color: white;
  max-width: 480px;
}

.form-check-label a {
  color: #EF4D32;
  text-decoration: none;
}

.form-check-label a:hover {
  text-decoration: underline;
}
.btn {
  width: 480px;
  height: 60px;
}
.e-mail {
  margin-top: 10px;
}

.footer {
  background-color: #040613;
  height: 200px;
}



</style>