<template>
  <b-container class="main-content">
    <b-row class="breadcrumb-row">
      <bread-crumbs :bread-crumb-items="breadCrumbItems" />
    </b-row>
    <page-title :page-title-text="pageTitleText" />

    <b-row>
      <b-col cols="12" class="menu-col">
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
    </b-row>

  </b-container>

</template>

<script>
import BreadCrumbs from "@/components/BreadCrumbs";
import PageTitle from "@/components/PageTitle";
import MenuList from "@/components/MenuList";
export default {
  name: "collections",
  components: {MenuList, PageTitle, BreadCrumbs},
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
}
</style>
