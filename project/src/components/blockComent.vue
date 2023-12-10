<template>
<div class="rectangle">
    <div class="rec_style1">
        <img src="imageadasd.png" class="picture_rec">
        <div class="rec_style2">
            <div class="drupal_coder">Команда Drupal Coder вызвала только положительные впечатления!</div>
            <div class="rec_style3">
                <div class="rec_style3_text">Нуреев Александр, менеджер проекта Winamp Russian Community</div>
            </div>
        </div>
        <div class="vector_l"><svg xmlns="http://www.w3.org/2000/svg" width="1" height="283" viewBox="0 0 1 283" fill="none">
            <path opacity="0.2" d="M0.5 0V282.5" stroke="black"/>
            </svg>
        </div>
        <div class="strelka_1">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="34" viewBox="0 0 18 34" fill="none">
                <path d="M17 1L1 17L17 33" stroke="#050C33"/>
              </svg>
        </div>
        <div class="pages">
            01 / 14
    </div>
    <div class="strelka_2">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="34" viewBox="0 0 18 34" fill="none">
            <path d="M1 1L17 17L1 33" stroke="#050C33"/>
          </svg>
    </div>

</div>
</div>
</template>
  
  <script>

  </script>
  
  <style scoped>
  .rectangle {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
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
            position: relative; /* Возвращаем position relative для .rec_style1 */
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
            color: var(--Gray-5, #E0E0E0);
            font-family: Montserrat;
            font-size: 28px;
            font-style: normal;
            font-weight: 400;
            line-height: 28px;
            margin-left: 756px;
            margin-top: 204px;
            position: absolute;
        }
  </style>