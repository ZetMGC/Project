    <template>
        <div>
        <h1>Команда</h1>
    
        <div class="team-container">
            <div class="image-container">
            <img src="../img/team_2.jpg" alt="1 тимейт">
            <p class="teamText1">Даня</p>
            <p class="teamText2">Студент КубГу</p>
            
            </div>
    
            <div class="image-container">
            <img src="../img/team_1.jpg" alt="2 тимейт">
            <p class="teamText1">Денис</p>
            <p class="teamText2">Студент КубГу</p>
        
            </div>
    
            <div class="image-container">
            <img src="../img/team_3.jpg" alt="3 тимейт">
            <p class="teamText1">Влад  </p>
            <p class="teamText2">Студент КубГу</p>
            </div>
        </div>
        <div class="team-container">
            <div class="image-container">
            <img src="../img/team_1.jpg" alt="1 тимейт">
            <p class="teamText1">Денис</p>
            <p class="teamText2">Студент КубГу</p>
            </div>
    
            <div class="image-container">
            <img src="../img/team_3.jpg" alt="2 тимейт">
            <p class="teamText1">Влад</p>
            <p class="teamText2">Студент КубГу</p>
            </div>
    
            <div class="image-container">
            <img src="../img/team_2.jpg" alt="3 тимейт">
            <p class="teamText1">Даня  </p>
            <p class="teamText2">Студент КубГу</p>
            </div>
        </div>
        </div>
    </template>
    
    <script>
    
    </script>
    
    <style scoped>
    .team-container {
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
        margin: 20px;
    }
    
    .image-container {
        text-align: center;
        margin: 10px;
    }
    
    .image-container img {
        width: 100%;
        max-width: 300px;
        height: auto;
        border-radius: 5px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    
    .image-container p {
        margin-left: 2%;
        text-align: left;
        margin-top: 5px;
    }
    
    h1 {
        color: var(--main-black, #050C33);
        text-align: center;
        font-family: Montserrat;
        font-size: 42px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        margin: 0;
    }
    
    body {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        margin: 0;
    }

    .teamText1{   
        color: var(--main-black, #050C33);
        font-family: Montserrat;
        font-size: 16px;
        font-style: normal;
        font-weight: 700;
        line-height: 22px; 
    }

    .teamText2{

        color: var(--main-black, #050C33);
    font-family: Montserrat;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 22px; 
    }

    @media only screen and (max-width: 600px)
    {
        h1 {
        color: var(--main-black, #050C33);
        text-align: none;
        font-family: Montserrat;
        font-size: 20px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        margin: 0;
    }
    .image-container img {
        width: 100%;
        max-width: 140px;
        height: auto;
        border-radius: 5px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    body {
        height: 50vh;
    }
    h1 {
      font-size: 20px;
    }
    .teamText1{
        font-size: 10px;
    }
    .teamText2{
        font-size: 10px;
    }
    }
    </style>
    