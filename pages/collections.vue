<template>
  <b-container class="main-content">
    <b-row class="breadcrumb-row">
      <bread-crumbs :bread-crumb-items="breadCrumbItems" />
    </b-row>
    <page-title :page-title-text="pageTitleText" />

    <b-row>
      <b-col cols="12" md="4" xl="3" class="menu-col">
        <menu-list :menu-list-items="collectionMenuList" class="collection-menu-list" />
        <b-dropdown
          :text="collectionMenuTitle"
          class="collection-Menu-dd"
          split
          toggle-class="list-button-dd"
          split-class="list-button">
          <b-dropdown-item-button
            class="collection-menu-button"
            v-for="menuItem in collectionMenuList"
            v-on:click="collectionMenuTitle = menuItem.text">
            {{menuItem.text}}
          </b-dropdown-item-button>
        </b-dropdown>
      </b-col>
      <b-col cols="12" md="8" xl="9" class="collection-col">
        <b-row class="collection-title-row">
          <b-col cols="12" xl="6" class="collection-title">Афиши</b-col>
          <b-col cols="12" xl="6" class="collection-num">Показано экспонатов: 1-12 из 774</b-col>
        </b-row>
        <b-row class="pagination-row">
          <pagination />
        </b-row>
        <b-row class="posters-row">

          <b-card class="poster-card" v-for="poster in posters">
            <div class="poster-card-img-cont">
              <b-card-img :src="poster.image" top class="poster-card-image">
              </b-card-img>
            </div>
            <b-card-text class="poster-card-text"><b-link to="collectionItem">{{poster.text}}</b-link></b-card-text>
          </b-card>
        </b-row>



      </b-col>
    </b-row>

  </b-container>

</template>

<script>
import BreadCrumbs from "@/components/BreadCrumbs";
import PageTitle from "@/components/PageTitle";
import MenuList from "@/components/MenuList";
import Pagination from "@/components/Pagination";
export default {
  name: "collections",
  components: {Pagination, MenuList, PageTitle, BreadCrumbs},
  data() {
    return {
      pageTitleText: 'Экспонаты',
      collectionMenuTitle: 'Афиши',
      breadCrumbItems: [
        {
          text: 'Главная',
          to: '/'
        },
        {
          text: 'Коллекции',
          active: true
        }
      ],
      collectionMenuList: [
        {text: "Афиши"},
        {text: "Декорации"},
        {text: "Документы, рукописи"},
        {text: "Здания театров и музеев"},
        {text: "Книги"},
        {text: "Костюмы, грим"},
        {text: "Куклы"},
        {text: "Награды"},
        {text: "Портреты"},
        {text: "Программы"},
        {text: "Реквизит, бутафория, предметы"},
        {text: "Скульптура"},
        {text: "Стенды"},
        {text: "Сцены из спектаклей"}
      ],
      posters: [
        {image: '~assets/img/posters/1.png', text: 'Афиша с исполнителями. Третья студия МХАТ (Студия Вахтангова). "Принцесса Турандот". 27 февраля 1922 г.'},
        {image: '~assets/img/posters/2.png', text: 'Акимов Николай Павлович (1901-1968). Афиша художественная с исполнителями. Ленинград, Ленинградский Большой драматический театр. "Продавцы славы" Паньоль М., Нивуа П. 12, 14, 16, 21 января 1926'},
        {image: '~assets/img/posters/3.png', text: 'Акимов Николай Павлович (1901-1968). Афиша художественная. Ленинград, Государственный академический театр драмы. "Радость" Щеглов Д.А. 17 декабря 1931 г.'},
        {image: '~assets/img/posters/1.png', text: 'Афиша с исполнителями. Третья студия МХАТ (Студия Вахтангова). "Принцесса Турандот". 27 февраля 1922 г.'},
        {image: '~assets/img/posters/2.png', text: 'Акимов Николай Павлович (1901-1968). Афиша художественная с исполнителями. Ленинград, Ленинградский Большой драматический театр. "Продавцы славы" Паньоль М., Нивуа П. 12, 14, 16, 21 января 1926'},
        {image: '~assets/img/posters/3.png', text: 'Акимов Николай Павлович (1901-1968). Афиша художественная. Ленинград, Государственный академический театр драмы. "Радость" Щеглов Д.А. 17 декабря 1931 г.'},
      ]
    }
  }
}
</script>

<style scoped>
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .main-content {
    padding-left: 15px;
    padding-right: 15px;
  }
  .menu-col {
    padding: 0;
  }
  .collection-menu-list {
    display: none;
  }
  .collection-Menu-dd {
    width: 100%;
    border: solid #cf6a40 3px;
  }
  .collection-col {
    padding-left: 0;
    padding-top: 30px;
  }

  .collection-title {
    font-size: 20px;
    font-weight: bold;
    padding: 0;
  }


  .collection-num {
    text-align: left;
    font-size: 14px;
    color: #9f959d;
    line-height: 2;
  }


  .pagination-row {
    text-align: center;
    padding-top: 20px;
    padding-bottom: 30px;

  }


  .posters-row {
    margin-bottom: 30px;
    margin-left: auto;
    margin-right: auto;
    padding: 0;
  }

  .poster-card {
    border: none;
    border-radius: 0;
    padding: 0 3px;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 20px;

  }
  .poster-card .card-body {
    padding: 0;
    text-align: center;
  }
  .poster-card-img-cont {
    background-color: #f5f2ec;
    width: 16vw;
    height: 16vw;
    min-height: 130px;
    min-width: 130px;
    padding: 0;
    display: flex;
    margin: auto;

  }

  .poster-card-image {
    object-fit: contain;

  }
  .poster-card-text {

    width: 16vw;
    min-width: 130px;
    max-height: 130px;
    overflow: hidden;
    margin: 15px auto auto;
    text-align: left;
  }
  .poster-card-text a{
    font-size: 16px;
    color: #270000 !important;
    font-weight: bold;
    text-decoration: underline;
    line-height: 1.625;

  }
  .poster-card-text:hover a{
    color: #d78d5e !important;
  }
}
/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {
  .collection-menu-list {
    display: flex;
  }
  .collection-Menu-dd {
    display: none;
  }
  .menu-col {
    border-right: solid #270000 1px;
  }
  .collection-col {
    padding-top: 0;
  }
  .collection-title {
    margin-left: 15px;
    font-size: 26px;
  }
  .collection-num {
    font-size: 16px;
  }
  .pagination-row {
    padding-top: 0;
    padding-bottom: 0;
  }
  .poster-card-img-cont {

    min-height: 190px;
    min-width: 180px;


  }

  .poster-card-text {

    min-height: 135px;
    min-width: 180px;

  }
  /* пк версия более 1024 px*/
  @media (min-width: 1024px) {
    .collection-title {
      margin-left: 0;
      padding-left: 30px;
    }
    .collection-num {
      text-align: right;
    }
    .collection-title-row {
      flex-direction: row;
    }
  }
  .poster-card-text {
    max-height: 180px;
  }




}
/* пк версия более 1024 px*/
@media (min-width: 1024px) {

}




</style>
