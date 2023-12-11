<template>
    <div id="header" class="row justify-content-center">
        <div class="col-8">
            <nav class="navbar navbar-expand-lg navbar-dark">
                <div class="container">
                    <router-link to="/" class="navbar-brand">
                        <img :src="require('@/img/Drupal.svg')" alt="Логотип">
                    </router-link>
          
                    <button
                    class="navbar-toggler"
                    type="button"
                    data-toggle="collapse"
                    data-target="#navbarNav"
                    aria-controls="navbarNav"
                    aria-expanded="false"
                    aria-label="Toggle navigation"
                    >
                    <span class="navbar-toggler-icon"></span>
                    </button>
                   <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav ml-auto">
                            <li class="nav-item">
                                <a to="/support" ref="support" id="support" class="nav-link">Поддержка Drupal</a>
                            </li>
                            <li class="nav-item">
                                <div class="dropdown" @mouseover="showDropdown" @mouseleave="hideDropdown">
                                    <a to="/admin" @mouseenter="onMenuMouseEnter" ref="admin" id="admin" role="button" class="nav-link dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">Администрирование</a>
                                    <ul ref="dropdownContent" class="dropdown-menu animated" @mouseover="onDropdownMouseOver" @mouseleave="hideDropdown" v-if="isDropdownVisible" aria-labelledby="admin">
                                        <li><a class="dropdown-item" href="#">Действие</a></li>
                                        <li><a class="dropdown-item" href="#">Другое действие</a></li>
                                        <li><a class="dropdown-item" href="#">Что-то еще здесь</a></li>
                                    </ul>
                                </div>
                            </li>
                            <li class="nav-item">
                                <a to="/promotion" ref="promotion" id="promotion" class="nav-link">Продвижение</a>
                            </li>
                            <li class="nav-item">
                                <a to="/ad" ref="ad" id="ad" class="nav-link">Реклама</a>
                            </li>
                            <li class="nav-item">
                                <a to="/about" ref="about" id="about" class="nav-link dropdown-toggle">О нас</a>
                            </li>
                            <li class="nav-item">
                                <a to="/projects" ref="projects" id="projects" class="nav-link">Проекты</a>
                            </li>
                            <li class="nav-item">
                                <a to="/contacts" ref="contacts" id="contacts" class="nav-link">Контакты</a>
                            </li>
                        </ul>
                    </div>
                </div> 
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
#header nav {
    background-color: transparent;
}

.dropdown {
  position: relative;
  display: inline-block;
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
    min-width: none;
    position: absolute;
    top: 100%;
    left: 0;
    z-index: 1000;
    max-width: fit-content;
    color: rgb(255, 255, 255);
    border-radius: 0;
    text-decoration: none;
    transition: display ;
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
</style>
  