<template>
    <h1>Тарифы</h1>
<div class="rectangles">
    <div class="rectangle">
        <div class="tarif_name">Стартовый</div>
        <div class="tarif_price">2000 ₽</div>
        <div class="tarif_chas">в час</div>
        <p class="tarif_vector">__________________________________ </p>
        
        <div class="tarif_content"> <div v-html="galka"></div>
        ㅤПредоплата от 2 часов</div>
        <div class="tarif_content"><div v-html="galka"></div>
        ㅤКонсультации и работы по SEO</div>
        <div class="tarif_content"><div v-html="galka"></div>
        ㅤУслуги дизайнера</div>
        <div class="tarif_content"><div v-html="galka"></div>
        ㅤСтандартное время реакции</div>
        <div class="tarif_content"><div v-html="galka"></div>
        ㅤНеиспользованные <br>оплаченные часы переносятся на следующий месяц</div>
        <div class="button-container">
            <button type="button" @click="OpenCloseFun()" :class="'btn btn-'+variant">Оставить заявку!</button>
        </div>
    </div>

    <div class="rectangle">
        <div class="tarif_name">Бизнес</div>
        <div class="tarif_price">2000 ₽</div>
        <div class="tarif_chas">в час</div>
        <p class="tarif_vector">__________________________________ </p>
        <div class="tarif_content"><div v-html="galka"></div>ㅤПредоплата от 10 часов</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤКонсультации и работы по SEO</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤУслуги дизайнера</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤВысокое время реакции –
            до 2 рабочих дней</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤНеиспользованные часы не переносятся</div>
        <div class="button-container">
            <button type="button" @click="OpenCloseFun()" :class="'btn btn-'+variant">Оставить заявку!</button>
        </div>
    </div>
    <div class="rectangle">
        <div class="tarif_name">VIP</div>   
        <div class="tarif_price">1800 ₽</div>
        <div class="tarif_chas">в час</div>
        <p class="tarif_vector">__________________________________ </p>
        <div class="tarif_content"><div v-html="galka"></div>ㅤПредоплата от 100 часов</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤКонсультации и работы по SEO</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤУслуги дизайнера</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤМаксимальное время реакции – <br>в день обращения</div>
        <div class="tarif_content"><div v-html="galka"></div>ㅤНеиспользованные часы не переносятся</div>
        <div class="button-container">
            <button type="button" @click="OpenCloseFun()" :class="'btn btn-'+variant" >Оставить заявку!</button>
        </div>
    </div>
</div>

  <div v-if="showModal" :style="{ opacity: modalOpacity, visibility: modalVisibility }" class="modal fade show" role="dialog" style="display: block" tabindex="-1" aria-labelledby="exampleModalLabel" aria-modal="true">
    <div class="modal-dialog" role="document">
      <div class="modal-content" style="background-color:#040613 ">
        <div class="modal-header">
          <h5 class="modal-title" style="color: white">Оставить заявку</h5>
        </div>
        <div class="modal-body">
          <div class="formDrupal col">
            <form @submit.prevent="submitForm()">
              <input type="text" v-model="formData.name" class="form-control" name="fullName" placeholder="Ваше имя" >
              <input type="tel" v-model="formData.number" class="form-control" name="phone" placeholder="Телефон" pattern="[0-9]+" required >
              <input type="email" v-model="formData.email" class="form-control" name="e-mail" placeholder="E-mail" >
              <textarea id="message" v-model="formData.comment" class="form-control" rows="4" placeholder="Ваш комментарий"></textarea>
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
          <button type="button" @click="OpenCloseFun()" :class="'btn btn-success'" >Закрыть</button>
          <button type="submit" class="btn btn-danger">Свяжитесь с нами</button>
        </div>
      </div>
    </div>
  </div>

<div class="rectangles2">
    <div class="tarif_zay1">Вам не подходят наши тарифы? Оставьте заявку и мы предложим вам индивидуальные условия!

    </div>
</div>
<div class="rectangles2">
    <div class="tarif_zay2">получить индивидуальный тариф
    </div>
</div>

  </template>
  
  <script>


        export default {
          data() {
            return{
              formData: {
                name: '',
                number: '',
                email: '',
                comment: ''
              },
              showModal: false,
              modalOpacity: 0,
              modalVisibility: 'hidden',
              isAnimating: false,
              galka: '<svg xmlns="http://www.w3.org/2000/svg" width="13" height="11" viewBox="0 0 13 11" fill="none" style="width: 13px; height: 10px; flex-shrink: 0;"><path d="M0.15 6C0.05 5.9 0 5.75 0 5.65C0 5.55 0.05 5.4 0.15 5.3L0.85 4.6C1.05 4.4 1.35 4.4 1.55 4.6L1.6 4.65L4.35 7.6C4.45 7.7 4.6 7.7 4.7 7.6L11.4 0.65H11.45C11.65 0.45 11.95 0.45 12.15 0.65L12.85 1.35C13.05 1.55 13.05 1.85 12.85 2.05L4.85 10.35C4.75 10.45 4.65 10.5 4.5 10.5C4.35 10.5 4.25 10.45 4.15 10.35L0.25 6.15L0.15 6Z" fill="#F69C8F"/></svg>'
            }
          },
          mounted() {
            const storedData = localStorage.getItem('formData');
            if (storedData) {
              this.formData = JSON.parse(storedData);
            }
          },
          beforeUnmount() {
            localStorage.setItem('formData', JSON.stringify(this.formData));
          },
          methods: {
            OpenCloseFun() {
              this.showModal = !this.showModal;
              if (this.showModal) {
                this.modalVisibility = 'visible';
              }
              this.animateModal();
            },
            openModal() {
              this.showModal = true;
              this.modalVisibility = 'visible';
              this.animateModal();
            },
            closeModal() {
              this.animateModal(false);
            },
            submitForm() {
              localStorage.removeItem('formData');
            },
            animateModal() {
              if (this.isAnimating) return;

              this.isAnimating = true;

              const startTime = performance.now();
              const duration = 500; // Длительность анимации в миллисекундах

              const animate = (currentTime) => {
                const progress = (currentTime - startTime) / duration;

                this.modalOpacity = this.showModal ? Math.min(progress, 1) : 1 - Math.min(progress, 1);

                if ((this.showModal && progress < 1) || (!this.showModal && progress > 0)) {
                  requestAnimationFrame(animate);
                } else {
                  if (!this.showModal) {
                    setTimeout(() => {
                      this.modalVisibility = 'hidden';
                      this.isAnimating = false;
                    }, 500); // Подстраивайте это значение в зависимости от длительности анимации
                  } else {
                    this.isAnimating = false;
                  }
                }
              };

              requestAnimationFrame(animate);
            },
          },
          watch: {
            visible:function(newVal, oldVal) {
              this.OpenClose = newVal
              console.log("new " + newVal + '===' + oldVal);
            }
          },
        }


  </script>
  
  <style scoped>
  .rectangles {
  margin-top:5%;
            display: flex;  
            justify-content: center;
            height: 690px;
            margin: 1;
        }
        .rectangles2 {
            display: flex;  
            justify-content: center;
            height: 60px;
            margin: 0;
        }
        .rectangle {
            border-radius: 5px;
            width: 390px;
            height: 619px;
            background-color: #3498db;
            margin: 0 10px;
            transition: all 0.3s ease;
            background: linear-gradient(0deg, rgba(255, 255, 255, 0.1), rgba(212, 212, 212, 0.1)), linear-gradient(0deg, #FFFFFF, #FFFFFF);
            border: 1px solid rgba(0, 0, 0, 0.1);
        }

        
        .rectangle:hover {
            width: 420px;
            height: 665px;
            box-shadow: 0px 4px 60px 0px rgba(161, 161, 161, 0.25);
        }


      

        .tarif_name {
            display: flex;
            justify-self: auto;
            font-weight: 900;
            color: rgba(241, 77, 52, 1);
            font-family: Montserrat;
            font-size: 22px;
            letter-spacing: 0em;
            text-align: left;
            margin-left: 15%;
            margin-top: 20%;
        }

        .tarif_price {
            width: 197.43px;
            height: 6%;
            color: rgba(5, 12, 51, 1);
            margin-top: 0;
            margin-left: 15%;
            font-family: Montserrat;
            font-size: 50px;
            font-weight: 700;
            letter-spacing: 0em;
            text-align: left;
        }

        .tarif_chas {
            
            font-weight: 900;
            font-family: Montserrat;
            font-size: 16px;
            line-height: 20px;
            letter-spacing: 0em;
            text-align: left;
            width: 125.35px;
            height: 18px;
            margin-top: 5%;
            margin-left: 15%;
        }
        .tarif_rub{
            font-weight: 900;
            font-family: Montserrat;
            font-size: 30px;
            line-height: 40px;
            letter-spacing: 0em;
            text-align: left;
            width: 125.35px;
            margin-top: -8%;
            margin-left: 48%;
        }
        .tarif_vector{
            display: flex;
            justify-content: center;
            color: #999999;
            
        }

        
        .tarif_content {
            display: flex;
            justify-self: stretch;
            font-family: Montserrat;
            font-size: 14px;
            font-weight: 500;
            line-height: 20px;
            letter-spacing: 0em;
            text-align: left;
            margin-left: 15%;
            margin-right: 16%;
            opacity: 0.7px;
            color: rgba(5, 12, 51, 1);
            margin-top: 5%;
            
        }

        .button-container {
           display: flex;
           justify-content: center;
           margin-top: 10%;
        }


        .button-container > button {
            padding: 15px;
            font-size: 30px;
            background-color: #ffffff;
            color: rgba(241, 77, 52, 1);;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            border: 1px solid rgba(241, 77, 52, 1);
            transition: background-color 0.3s ease;
        }

        .button-container > button:hover {
            background-color: rgba(241, 77, 52, 1);
            color: #ffffff;
        }
        
        .tarif_zay1{
            width: 468px;
            color: var(--main-black, #050C33);
            text-align: center;
            /* text/16px */
            font-family: Montserrat;
            font-size: 16px;
            font-style: normal;
            font-weight: 500;
            line-height: 22px; /* 137.5% */
            opacity: 0.5;
            
        }
        .tarif_zay2{
                color: var(--main-black, #050C33);
            text-align: center;
            font-family: Montserrat;
            font-size: 12px;
            font-style: normal;
            font-weight: 500;
            line-height: 12px; /* 100% */
            letter-spacing: 0.72px;
            text-decoration-line: underline;
            text-transform: uppercase;
            }
            h1 {
                margin-top: 10%;
                color: var(--main-black, #050C33);
                text-align: center;
            font-family: Montserrat;
            font-size: 42px;
            font-style: normal;
            font-weight: 700;
            line-height: normal;
            margin: 1;
    }

            @media only screen and (max-width: 600px){
                .rectangles{
                    flex-direction: column;
                    height: auto;
                }
                .rectangle {
                 width: 100%;
                 margin: 0 0 25px 0;
                }
                .rectangle:hover{
                    width: 100%;
                    height: 1;
                }
                
            }



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
  .modal-footer > .btn {
    height: 60px;
  }

  </style>
  