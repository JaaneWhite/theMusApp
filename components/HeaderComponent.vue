<template>
  <header>
    <b-row class="header-row">
      <!--слайдер с картинками -->
      <b-row class="header-carousel-row">
        <b-col cols="6" class="header-left">
        </b-col>
        <b-col cols="6" xl="6" class="header-right">
          <b-carousel class="header-carousel"
                      id="carousel-1"
                      v-model="slide"
                      :interval="4000"
          >
            <b-carousel-slide class="slide-img"
                              img-src="~assets/img/slider-1.png">
            </b-carousel-slide>
            <b-carousel-slide class="slide-img"
                              img-src="~assets/img/slider-2.png">
            </b-carousel-slide>
            <b-carousel-slide class="slide-img"
                              img-src="~assets/img/slider-3.png">
            </b-carousel-slide>

          </b-carousel>
        </b-col>
      </b-row>
      <b-row class="header-content">
        <b-container >
          <!--верхнее меню - бургер -->
          <b-row class="burger-menu-row">
          <ToggleMenu />
        </b-row>
          <b-row class="project-text-top">
            {{projectText}}
          </b-row>
          <!-- основной блок с заголовком и поиском -->
          <b-row class="header-content-row">
            <b-col cols="12" xl="7" class="title-col">
              <b-row class="project-text-center">{{projectText}}</b-row>
              <b-row class="title-text">ТЕАТРАЛЬНЫЕ МУЗЕИ И АРХИВЫ РОССИИ <br>И РУССКОГО ЗАРУБЕЖЬЯ</b-row>
            </b-col>
            <b-col cols="12" xl="1" class="empty-block"></b-col>
            <b-col cols="12" xl="4" class="search-block">
              <b-row class="search-row">
                <b-form class="search-form">
                  <b-form-input id="search-input" placeholder="Поиск" type="search"></b-form-input>
                  <b-button class="search-button keyboard-button"></b-button>
                  <b-img src="~assets/img/divider.png" class="divider-img"></b-img>
                  <b-button class="search-button sb-button"></b-button>
                </b-form>
              </b-row>
          <b-row class="link-row">
            <b-col cols="9" class="left-link"><b-link to="#" class="search-link">Расширенный поиск</b-link></b-col>
            <b-col cols="3" class="right-link"><b-link to="#" class="search-link">А - Я</b-link></b-col>
          </b-row>
        </b-col>
        </b-row>
      </b-container>
      </b-row>
    </b-row>
    <!-- развернутое меню для планшетной и пк-версий -->
    <b-row class="menu-row">
      <b-container>
       <TopMenu/>
      </b-container>
    </b-row>

  </header>
</template>

<script>
import TopMenu from "~/components/TopMenu";
import ToggleMenu from "~/components/ToggleMenu";
export default {
  name: "HeaderComponent",
  components: {ToggleMenu, TopMenu},
  data() {
    return {
      projectText: "Проект осуществлён на средства гранта Президента Российской Федерации. Программа для поддержки творческих проектов общенационального значения в области культуры и искусства области культуры.",
    }
    }
}
</script>

<style scoped>
/* мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .header-row {
    height: 429px;
    background-image: url("~assets/img/header bg.png");
  }
  .header-carousel-row {
    display: none;
  }

  .burger-menu-row {
    height: 80px;
  }
  .project-text-center {
    display: none;
  }
  .title-col {
    display: flex;
  }

  .title-text {
    color: white;
    font-size: 22px;
    text-align: left;
    line-height: 1.389;
    margin: 60px 0 45px 0;
  }


  .empty-block {
    padding: 0;
  }

  .search-block {
    display: flex;
    text-align: right;
    flex-direction: column;
    margin-top: 4vw;
  }

  .search-row {
    margin: 0;
  }

  .search-form {
    text-align: right;
    display: flex;
    margin-right: 0;
    margin-left: 0;
    width: 100%;
    border-radius: 25px;
    opacity: 75%;
    height: 44px;
    padding: 0 20px 0 10px;
    background-color: white;

  }

  .search-form:active, .search-form:focus, .search-form:hover {
    opacity: 100%;
  }

  .search-button {
    background-color: transparent;
    border: none;
    background-repeat: no-repeat;
    background-position: center;
  }

  .keyboard-button {
    display: none;
  }

  .sb-button {
    background-image: url("~assets/img/search.png");
  }

  .sb-button:active, .sb-button:hover, .sb-button:focus {
    background-image: url("~assets/img/search r.png");
  }

  .divider-img {
    display: none;

  }

  #search-input {
    color: #31112C !important;
    height: 100%;
    font-style: italic;
    font-size: 14px;
    line-height: 1.2;
    border: none;
    box-shadow: none;
    background-color: transparent;
  }

  .link-row {
    margin: 10px 0 0;
    text-align: left;

  }

  .search-link {
    color: white !important;
    text-decoration: none;
    border-bottom: dotted 2px;
    font-size: 14px;
    line-height: 2.143;
    text-shadow: 0 0 1px rgba(39, 0, 0, 0.004);
  }

  .left-link {
    padding: 0;
  }

  .right-link {
    text-align: right;
    padding: 0;
  }
}

/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {
  .header-row {
    height: 474px;
  }
  .burger-menu-row {
    display: none;
  }
  .keyboard-button {
    display: inline-block;
    background-image: url("~assets/img/keyboard.png");
  }
  .divider-img {
    display: inline-block;
    margin: 5px;
  }
  .title-text {
    font-size: 30px;
    text-align: center;
    line-height: 1.333;
    margin: 60px auto 45px auto;
  }
  .project-text-top {
    display: flex;
    text-align: center;
    font-size: 12px;
    color: white;
    padding-top: 30px;
    padding-left: 115px;
    padding-right: 115px;
  }
  .search-block {
    padding-left: 20%;
    padding-right: 20%;
  }
  .menu-row {
    display: flex;
    background-color: #e5d1b3;
    height: 60px;
  }

}

/* пк версия - 1024 - ... px*/
@media (min-width: 1024px) {
  .header-row {
    height: 453px;

  }
  .header-carousel-row {
    display: contents;
    height: 453px;
  }
  .header-content {
    position: absolute;
    z-index: 10;
    top: 0;
    width: 100%;
  }
  .header-content-row {
    flex-direction: row;
    padding-top: 45px;
  }
  .search-block {
    padding: 0;
    margin-top: 0;
  }
  .header-left {
    padding: 0;

  }
  .header-right {
    display: flex;
    text-align: right;
    padding: 0;
  }
  .header-carousel {
    height: 453px;
    clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 0% 100%);
  }
  .project-text-top {
    display: none;
  }
  .project-text-center {
    display: flex;
    color: white;
    font-size: 14px;
    text-align: left;
    padding-left: 0;

  }
  .title-col {
    padding-left: 0;
    flex-direction: column;
  }
  .title-text {
    font-size: 36px;
    line-height: 1.389;
    text-align: left;
    padding: 0;
    margin-left: 0;
    margin-top: 100px;
  }
  .menu-row {
    z-index: 20;

  }
}



</style>
