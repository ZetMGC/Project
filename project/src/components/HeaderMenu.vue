<template>
    <div id="header" class="">
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
                        <router-link to="/support" class="nav-link">Поддержка сайтов</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/pricing" class="nav-link">Тарифы</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/portfolio" class="nav-link">Наши работы</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/reviews" class="nav-link">Отзывы</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/contact" class="nav-link">Контакты</router-link>
                    </li>
                    </ul>
                </div>
                <div class="ml-auto d-flex align-items-center">
                    <div class="mx-4 number-text">8 800 222-26-73</div>
                    <div class="language-dropdown" @mouseover="showDropdown" @mouseleave="hideDropdown">
                        <button
                          ref="dropdownButton"
                          class="btn btn-secondary dropdown-toggle"
                          type="button"
                          aria-haspopup="true"
                          aria-expanded="false"
                        >
                          {{ selectedLanguage }}
                        </button>
                        <ul class="dropdown-menu w-60" aria-labelledby="languageDropdown">
                            <li><a @click="changeLanguage('RU')" class="dropdown-item" href="#">RU</a></li>
                            <li><a @click="changeLanguage('EN')" class="dropdown-item" href="#">EN</a></li>
                        </ul>
                      </div>
                </div>
            </div>
        </nav>
    </div>
</template>
  
<script>
import * as bootstrap from 'bootstrap/dist/js/bootstrap.bundle.min.js';
export default {
  name: 'LanguageSelector',
  data() {
    return {
      selectedLanguage: 'RU',
      isDropdownVisible: false
    };
  },
  methods: {
    changeLanguage(language) {
        this.selectedLanguage = language;
    },
    showDropdown() {
        this.isDropdownVisible = true;
    },
    hideDropdown() {
        this.isDropdownVisible = false;
    },
    activateDropdown() {
        new bootstrap.Dropdown(this.$refs.dropdownButton);
    }
  },
  mounted() {
    this.activateDropdown();
  }
};
</script>
  
<style scoped>
#header nav {
    background-color: transparent;
}

.number-text {
    color: #FFF;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 14px;
}

.language-dropdown {
    position: relative; 
}

.dropdown-menu, ul.dropdown-menu {
    display: none;
    background-color: transparent;
    border: none;
    min-width: none;
    position: absolute;
    top: 100%;
    left: 0;
    z-index: 1000;
    max-width: fit-content;
    width: 60px;
}

.dropdown-menu li a, .dropdown-menu li {
    width: fit-content;
    color: #FFF;
}
  
.language-dropdown:hover .dropdown-menu {
    display: block;
    color: #000;
}

.btn-secondary {
    background-color: transparent;
    border-color: transparent;
  }
  
</style>
  