
<template>
  <div v-if="OpenClose" class="modal fade show" role="dialog" style="display: block" tabindex="-1" aria-labelledby="exampleModalLabel" aria-modal="true">
    <div class="modal-dialog" role="document">
      <div class="modal-content" style="background-color:#040613 ">
        <div class="modal-header">
          <h5 class="modal-title" style="color: white">Оставить заявку</h5>
        </div>
        <div class="modal-body">
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
            </form>
          </div>
        </div>
        <div class="modal-footer">
          <button type="button" @click="OpenCloseFun()" :class="'btn btn-'+variant" >Закрыть</button>
          <button type="button" class="btn btn-danger">Свяжитесь с нами</button>
        </div>
      </div>
    </div>
  </div>
  <button type="button" @click="OpenCloseFun()" :class="'btn btn-'+variant" >Open</button>
</template>

<script>
export default {
  name:"ModalTest",
  props: {
    visible: Boolean,
    variant: String,
  },
  data() {
    return{
      OpenClose: this.visible
    }
  },
  methods:{
    OpenCloseFun() {
      this.OpenClose = !this.OpenClose;
    }
  },
  watch: {
    visible:function(newVal, oldVal) {
      this.OpenClose = newVal
      console.log("new " + newVal + '===' + oldVal);
    }
  }
}
</script>

<style scoped>


.formDrupal > form {
  padding: 10px;
}
.formDrupal > form > .form-control{
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
  margin-top: 10px;
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
  height: 60px;
}

</style>
