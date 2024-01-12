<template>
  <h1 style="margin-bottom: 20px">Отзывы</h1>
  <h2><svg xmlns="http://www.w3.org/2000/svg" width="212" height="437" viewBox="0 0 212 437" fill="none">
  <path d="M186.719 0.919922H33.0095C19.0543 0.919922 7.7284 12.2459 7.7284 26.201V179.91C7.7284 193.866 19.0543 205.191 33.0095 205.191H106.578C105.617 245.439 96.2629 277.647 78.5661 301.866C64.6109 320.979 43.4764 336.805 15.2116 349.294C2.2171 355.007 -3.3953 370.378 2.67217 383.221L20.8746 421.649C26.7398 433.985 41.2512 439.396 53.7906 433.985C87.2628 419.525 115.528 401.221 138.583 378.974C166.697 351.822 185.96 321.181 196.376 287.001C206.792 252.821 212 206.203 212 147.045V26.201C212 12.2464 200.673 0.919922 186.719 0.919922Z" fill="#050C33"/>
</svg></h2>
<h3><svg xmlns="http://www.w3.org/2000/svg" width="212" height="437" viewBox="0 0 212 437" fill="none">
  <path d="M186.719 0.919922H33.0095C19.0543 0.919922 7.7284 12.2459 7.7284 26.201V179.91C7.7284 193.866 19.0543 205.191 33.0095 205.191H106.578C105.617 245.439 96.2629 277.647 78.5661 301.866C64.6109 320.979 43.4764 336.805 15.2116 349.294C2.2171 355.007 -3.3953 370.378 2.67217 383.221L20.8746 421.649C26.7398 433.985 41.2512 439.396 53.7906 433.985C87.2628 419.525 115.528 401.221 138.583 378.974C166.697 351.822 185.96 321.181 196.376 287.001C206.792 252.821 212 206.203 212 147.045V26.201C212 12.2464 200.673 0.919922 186.719 0.919922Z" fill="#050C33"/>
</svg></h3>
    <div class="rectangle">
      <div class="rec_style1">
        <img src="../img/image01.png" class="picture_rec">
        <div class="rec_style2">
          <div class="drupal_coder">{{ getContent(currentPage) }}</div>
          <div class="rec_style3">
            <div class="rec_style3_text">{{ getAuthor(currentPage) }}</div>
          </div>
        </div>  
        <div class="vector_l">
          <svg xmlns="http://www.w3.org/2000/svg" width="1" height="283" viewBox="0 0 1 283" fill="none">
            <path opacity="0.2" d="M0.5 0V282.5" stroke="black"/>
          </svg>
        </div>
        <div class="strelka_1" @click="changePage(-1)">
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="34" viewBox="0 0 18 34" fill="none">
            <path d="M17 1L1 17L17 33" stroke="#050C33"/>
          </svg>
        </div>
        <div class="pages" id="pageNumber">
          {{ currentPage.toString().padStart(2, '0') }} / 6
        </div>
        <div class="strelka_2" @click="changePage(1)">
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="34" viewBox="0 0 18 34" fill="none">
            <path d="M1 1L17 17L1 33" stroke="#050C33"/>
          </svg>
        </div>
      </div>
    </div>
  </template>
  
<script>
export default {
  data() {
    return {
      currentPage: 1,

    };
  },
  methods: {
    changePage(delta) {
      this.currentPage += delta;
      this.currentPage = Math.max(1, Math.min(this.currentPage, 6));
    },
    getContent(page){
      const contents= [
      "Команда Drupal Coder вызвала только положительные впечатления!",
      "Пушечка","Легендарный сайт","","Для чего","Крутящий момент","Контент 7","Контент 8","Контент 9","Контент 10","Контент 11","Контент 12","Контент 13","Контент 14"
      ];
      return contents[page-1] || "";
    },
    getAuthor(page){
      const authors=[
    "Нуреев Александр, менеджер проекта Winamp Russian Community",
    "Сиротин Владислав","Даня Леонтьев","Денис Муха","Денис я не знаю","Марат Калинов","Автор 7","Автор 8","Автор 9","Автор 10","Автор 11","Автор 12","Автор 13","Автор ё1"
      ];
      return authors[page-1] || "";
    }
  },
};


</script>
  
  <style scoped>
  h3{
    margin-top: -5%;
    margin-left: -5%;
    width: 211.773px;
    height: 435.16px;
    flex-shrink: 0;
    fill: var(--main-black, #050C33);
    position: absolute;
    opacity: 0.3;

  }
  h2{
    margin-top: -5%;
    margin-left: 20%;
    width: 211.773px;
    height: 435.16px;
    flex-shrink: 0;
    fill: var(--main-black, #050C33);
    position: absolute;
    opacity: 0.3;
  }
  .rectangle {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 50vh;
            margin: 0;
            position: relative;
            
        }

        .picture_rec {
            width: 200px;
            height: 46px;
            flex-shrink: 0;
            margin-top: 80px;
            margin-left: 128px;
            position: absolute;
        }

        .rec_style3 {
            width: 380px;
            height: 46px;
            flex-shrink: 0;
            margin-left: 0px;
            margin-top: 130px;
            position: absolute;
        }

        .rec_style3_text {
            opacity: 0.5;
            width: 380px;
            height: 46px;
            flex-shrink: 0;
            color: var(--main-black, #050C33);
            font-family: Montserrat;
            font-size: 14px;
            font-style: normal;
            font-weight: 500;
            line-height: normal;
            position: absolute;
        }

        .rec_style2 {
            width: 440px;
            height: 87px;
            margin-left: 128px;
            margin-top: 167px;
            margin-right: 412px;
            margin-bottom: 162px;
            position: absolute;
        }

        .rec_style1 {

            width: 980px;
            height: 416px;
            border-radius: 5px;
            border: 1px solid rgba(0, 0, 0, 0.10);
            background: #FFF;
            box-shadow: 0px 4px 60px 0px rgba(161, 161, 161, 0.25);
            position: relative; 
        }

        .drupal_coder {
            width: 440px;
            color: var(--main-black, #050C33);
            font-family: Montserrat;
            font-size: 24px;
            font-style: normal;
            font-weight: 700;
            line-height: normal;
            text-decoration-line: underline;
            position: absolute;
        }

        .vector_l {
            margin-top: 67px;
            margin-left: 628.5px;
            width: 0px;
            height: 282.5px;
            stroke-width: 1px;
            stroke: #000;
            opacity: 1.;
            position: absolute;
        }

        .strelka_1{
            width: 16px;
            height: 32px;
            
            flex-shrink: 0;
            stroke-width: 1px;
            stroke: var(--main-black, #050C33);
            margin-top: 202px;
            margin-left: 694px;
            position: absolute;
        }
        .strelka_2{
            width: 16px;
            height: 32px;
            flex-shrink: 0;
            stroke-width: 1px;
            stroke: var(--main-black, #050C33);
            margin-left: 884px;
            margin-top: 202px;
            position: absolute;
        }
        .pages{
            color: var(--main-black, #050C33);
            font-family: Montserrat;
            font-size: 28px;
            font-style: normal;
            font-weight: 400;
            line-height: 28px; /* 100% */
            font-family: Montserrat;
            font-size: 28px;
            font-style: normal;
            font-weight: 400;
            line-height: 28px;
            margin-left: 756px;
            margin-top: 204px;
            position: absolute;
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

        @media only screen and (max-width: 700px) {
          h2{
            display: none
          }
          h3{
            display: none
          }
            .rectangle {
              height: auto;
            }
            .picture_rec {
              width: 100%;
              max-width: 200px; 
              height: auto;
              margin-top: 20px;
              margin-left: 10px;
              position: static;
            }
            .rec_style3 {
              width: 100%;
              max-width: 380px;
              height: auto;
              margin-left: 0;
              margin-top: 20px;
              position: static;
            }
            .rec_style3_text {
              width: 100%;
              max-width: 380px; 
              height: auto;
              margin-top: 10px;
              position: static;
            }

            .rec_style2 {
              width: 100%;
              max-width: 440px; 
              height: auto;
              margin-left: 0;
              margin-top: 20px;
              margin-right: 0;
              margin-bottom: 20px;
              position: static;
            }

            .rec_style1 {
              width: 95%;
              height: auto;
            }
            .drupal_coder {
              width: 100%;
              font-size: 18px;
              line-height: 1.5; 
              position: static;
            }
            .pages{
            color: var(--main-black, #050C33);
            font-family: Montserrat;
            font-size: 28px;
            font-style: normal;
            font-weight: 400;
            line-height: 28px; /* 100% */
            font-family: Montserrat;
            font-size: 28px;
            font-style: normal;
            font-weight: 400;
            line-height: 28px;
            margin-left: 40%;
            margin-top: 2px;
        }
        .strelka_1{
          width: 16px;
      height: 32px;
      flex-shrink: 0;
      stroke-width: 1px;
      stroke: var(--main-black, #050C33);
      position: absolute; 
      margin-top: 0px; 
      margin-left: 30%;
      margin-right: auto;
      display: block;
        }
    .strelka_2 {
      width: 16px;
      height: 32px;
      flex-shrink: 0;
      stroke-width: 1px;
      stroke: var(--main-black, #050C33);
      position: relative; 
      margin-top: 10px; 
      margin-left: 62%;
      margin-right: auto;
      display: block;
    }
        .vector_l {
            margin-top: 0px;
            margin-left: 0PX;
            width: 0px;
            height: 282.5px;
            stroke-width: 0px;
            stroke: #000;
            opacity: 0.;
            position: absolute;
        }
          }

  </style>