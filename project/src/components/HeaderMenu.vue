<template>
    <div id="header" class="row justify-content-center">
        <div class="col-12 col-xl-7 custom-col">
            <nav class="navbar navbar-expand-sm navbar-expand-md navbar-dark" id="lgHeader">
                <div class="container">

                  <a class="navbar-brand" href="#">
                    <img class="navbar-brand" :src="require('@/img/Drupal.svg')" alt="Логотип">
                  </a>

                    <button
                    class="navbar-toggler"
                    type="button"
                    data-bs-toggle="collapse"
                    data-bs-target="#navbarNav"
                    aria-controls="navbarNav"
                    aria-expanded="false"
                    aria-label="Toggle navigation"
                    >
                    <span class="navbar-toggler-icon"></span>
                    </button>

                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav sm-fixed-bottom ml-auto">
                            <li class="nav-item">
                                <a to="/support" ref="support" id="support" class="nav-link">ПОДДЕРЖКА DRUPAL</a>
                            </li>
                            <li class="nav-item">
                                <div class="dropdown" @mouseover="showDropdown" @mouseleave="hideDropdown">
                                    <a to="/admin" @mouseenter="onMenuMouseEnter" ref="admin" id="admin" role="button" class="nav-link dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">АДМИНИСТРИРОВАНИЕ</a>
                                    <ul ref="dropdownContent" class="dropdown-menu animated" @mouseover="onDropdownMouseOver" @mouseleave="hideDropdown" v-if="isDropdownVisible" aria-labelledby="admin">
                                        <li><a class="dropdown-item" href="#">МИГРАЦИЯ</a></li>
                                        <li><a class="dropdown-item" href="#">БЭКАПЫ</a></li>
                                        <li><a class="dropdown-item" href="#">АУДИТ БЕЗОПАСНОСТИ</a></li>
                                        <li><a class="dropdown-item" href="#">ОПТИМИЗАЦИЯ СКОРОСТИ</a></li>
                                        <li><a class="dropdown-item" href="#">ПЕРЕЕЗД НА HTTPS</a></li>
                                    </ul>
                                </div>
                            </li>
                            <li class="nav-item">
                                <a to="/promotion" ref="promotion" id="promotion" class="nav-link">ПРОДВИЖЕНИЕ</a>
                            </li>
                            <li class="nav-item">
                                <a to="/ad" ref="ad" id="ad" class="nav-link">РЕКЛАМА</a>
                            </li>
                            <li class="nav-item">
                                <div class="dropdown" @mouseover="showDropdown" @mouseleave="hideDropdown">
                                    <a to="/about" @mouseenter="onMenuMouseEnter" ref="about" id="about" role="button" class="nav-link dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">О НАС</a>
                                    <ul ref="dropdownContent" class="dropdown-menu animated" @mouseover="onDropdownMouseOver" @mouseleave="hideDropdown" v-if="isDropdownVisible" aria-labelledby="admin">
                                        <li><a class="dropdown-item" href="#">КОМАНДА</a></li>
                                        <li><a class="dropdown-item" href="#">DRUPALGIVE</a></li>
                                        <li><a class="dropdown-item" href="#">КУРСЫ DRUPAL</a></li>
                                        <li><a class="dropdown-item" href="#">ВАКАНСИИ</a></li>
                                    </ul>
                                </div>
                            </li>
                            <li class="nav-item">
                                <a to="/projects" ref="projects" id="projects" class="nav-link">ПРОЕКТЫ</a>
                            </li>
                            <li class="nav-item">
                                <a to="/contacts" ref="contacts" id="contacts" class="nav-link">КОНТАКТЫ</a>
                            </li>
                        </ul>
                    </div>
                </div> 
            </nav>

            <nav class="navbar px-4 fixed-bottom navbar-dark" id="smHeader">
              <div class="container">
                <div class="collapse navbar-collapse" id="navbarNav">
                  <ul class="navbar-nav sm-fixed-bottom ml-auto">
                    <li class="nav-item">
                      <a to="/support" ref="support" id="support" class="nav-link">ПОДДЕРЖКА DRUPAL</a>
                    </li>
                    <li class="nav-item">
                      <div class="accordion-item">
                        <h2 class="accordion-header" id="panelsStayOpen-headingOne">
                          <a class="accordion-button dropdown-toggle" type="button" data-bs-toggle="collapse" data-bs-target="#adminPanel" aria-expanded="true" aria-controls="panelsStayOpen-collapseOne">
                            АДМИНИСТРИРОВАНИЕ
                          </a>
                        </h2>
                        <div id="adminPanel" class="accordion-collapse collapse" aria-labelledby="panelsStayOpen-headingOne">
                          <ul ref="dropdownContent" class="accordion-body" aria-labelledby="admin">
                            <li><a class="dropdown-item" href="#">МИГРАЦИЯ</a></li>
                            <li><a class="dropdown-item" href="#">БЭКАПЫ</a></li>
                            <li><a class="dropdown-item" href="#">АУДИТ БЕЗОПАСНОСТИ</a></li>
                            <li><a class="dropdown-item" href="#">ОПТИМИЗАЦИЯ СКОРОСТИ</a></li>
                            <li><a class="dropdown-item" href="#">ПЕРЕЕЗД НА HTTPS</a></li>
                          </ul>
                        </div>
                      </div>
                    </li>
                    <li class="nav-item">
                      <a to="/promotion" ref="promotion" id="promotion" class="nav-link">ПРОДВИЖЕНИЕ</a>
                    </li>
                    <li class="nav-item">
                      <a to="/ad" ref="ad" id="ad" class="nav-link">РЕКЛАМА</a>
                    </li>
                    <li class="nav-item">
                      <div class="accordion-item">
                        <h2 class="accordion-header" id="panelsStayOpen-headingOne">
                          <a class="accordion-button dropdown-toggle" type="button" data-bs-toggle="collapse" data-bs-target="#panelAbout" aria-expanded="true" aria-controls="panelsStayOpen-collapseOne">
                            О НАС
                          </a>
                        </h2>
                        <div id="panelAbout" class="accordion-collapse collapse" aria-labelledby="panelsStayOpen-headingOne">
                          <ul ref="dropdownContent" class="accordion-body" aria-labelledby="admin">
                            <li><a class="dropdown-item" href="#">КОМАНДА</a></li>
                            <li><a class="dropdown-item" href="#">DRUPALGIVE</a></li>
                            <li><a class="dropdown-item" href="#">КУРСЫ DRUPAL</a></li>
                            <li><a class="dropdown-item" href="#">ВАКАНСИИ</a></li>
                          </ul>
                        </div>
                      </div>
                    </li>
                    <li class="nav-item">
                      <a to="/projects" ref="projects" id="projects" class="nav-link">ПРОЕКТЫ</a>
                    </li>
                    <li class="nav-item">
                      <a to="/contacts" ref="contacts" id="contacts" class="nav-link">КОНТАКТЫ</a>
                    </li>
                  </ul>
                </div>
              </div>

              <img class="navbar-brand" :src="require('@/img/Drupal.svg')" alt="Логотип">

              <button
                    class="navbar-toggler"
                    type="button"
                    data-bs-toggle="collapse"
                    data-bs-target="#navbarNav"
                    aria-controls="navbarNav"
                    aria-expanded="false"
                    aria-label="Toggle navigation"
                >
                  <span class="navbar-toggler-icon"></span>
                </button>
            </nav>
        </div>
    </div>
</template>
  
<script>

export default {
    components: {
        
    },
    data() {
        return {
            isDropdownVisible: false,
            hideDropdownTimeout: null
        };
    },
    methods: {
      showDropdown() {
        clearTimeout(this.hideDropdownTimeout);
        this.isDropdownVisible = true;
      },
      hideDropdown() {
        this.hideDropdownTimeout = setTimeout(() => {
          this.isDropdownVisible = false;
        }, 300); // Меняем таймаут на 300 миллисекунд
      },
      onDropdownMouseOver() {
        // Если мышь внутри меню, не скрывать его
        clearTimeout(this.hideDropdownTimeout);
      },
      onMenuMouseEnter() {
        // При наведении на ссылку "Меню", не скрывать меню
        clearTimeout(this.hideDropdownTimeout);
      }
    }
};
</script>
  
<style scoped>
a {
  font-size: 12px;
  text-decoration: none;
  font-family: Montserrat;
  font-weight: 500;
  transition: border 0.1s ease-in-out;
}

#smHeader ul {
  padding: 10px;
}

#smHeader ul.accordion-body {
  padding: 0px 0px 0px 8px;
}

a.accordion-button {
  padding-top: 8px;
  padding-bottom: 8px;
}

a.dropdown-item {
  padding-top: 8px;
  padding-bottom: 8px;
}

li {
  list-style-type: none;
}

#lgHeader #navbarNav {
  margin-top: 10px;
}

#lgHeader {
  background-color: transparent;
  display: none;
}

@media screen and (min-width: 690px) {
  .dropdown {
    position: relative;
    display: inline-block;
  }

  .navbar-brand {
    padding: 0px;
  }

  img.navbar-brand {
    padding: 10px 0px 0px 0px;
  }

  .nav-link.dropdown-toggle:hover {
    border-bottom: 0 solid transparent;
  }

  .nav-link {
    color: #FFF;
    cursor: pointer;
    border-bottom: 0px solid transparent;
  }

  .nav-link:hover {
    border-bottom: 3px solid #EF4D35;
  }

  .dropdown-menu {
    display: none;
    background-color: #EF4D35;
    border: none;
    min-width: 0;
    position: absolute;
    top: 100%;
    left: 0;
    z-index: 1000;
    max-width: fit-content;
    color: rgb(255, 255, 255);
    border-radius: 0;
    text-decoration: none;
  }

  .dropdown-menu a {
    color: #FFF;
  }

  .animated {
    animation: fadeIn 0.3s ease-in-out; /* Добавляем анимацию fadeIn */
  }

  .dropdown:hover .dropdown-menu {
    display: block;
    animation: fadeIn 0.3s ease-in-out;
  }

  .dropdown-menu a:hover {
    background-color: #CF3018;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
}

@media (min-width: 690px) {
  #lgHeader {
    display: block;
  }
  #smHeader {
    display: none;
  }
}


@media (min-width: 1450px) and (max-width: 1700px) {
  .custom-col {
    width: 70%; /* Например, 25% ширины экрана */
  }
}

@media (min-width: 1200px) and (max-width: 1450px) {
  .custom-col {
    width: 80%; /* Например, 25% ширины экрана */
  }
}

@media (min-width: 690px) and (max-width: 1000px) {
  .custom-col {
    width: 100%; /* Например, 25% ширины экрана */
  }
  .container {
    margin: 0;
  }
}

#smHeader {
  background-color: black;
}

#smHeader a {
  color: white;
  cursor: pointer;
}

#smHeader button{
  border: none;
}

#smHeader .dropdown-menu a:hover {
  background-color: black;
}

#smHeader .navbar-nav .dropdown-menu  {
  background-color: black;
  border-radius: 0;
  margin-top: 0px;
  padding: 0px;
}

#smHeader .nav-link, .accordion-button {
  border-bottom: 1px solid #312A2A;
}

@keyframes sliding {
  from {
    height: 0%;
  }
  to {
    height: 100%;
  }
}

#smHeader .dropdown-item {
  border-bottom: 1px solid #312A2A;
}

</style>
  