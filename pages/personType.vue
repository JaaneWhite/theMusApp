<template>
  <b-container class="main-content">
    <b-row class="breadcrumb-row">
      <bread-crumbs :bread-crumb-items="breadCrumbItems"/>

    </b-row>
    <page-title :page-title-text="pageTitle"/>
    <b-row class="person-date">
      <p>(англ. George Gordon Byron (Noel))</p>
      <p>(22 января 1788 года, Лондон — 19 апреля 1824 года, Миссолунги, Османская Греция)</p>
    </b-row>
    <b-row class="person-text">Английский поэт-романтик. Наряду с Перси Шелли и Джоном Китсом представляет младшее поколение британских романтиков. Его альтер-эго Чайльд-Гарольд стал прототипом бесчисленных байронических героев в литературе разных стран Европы.</b-row>
    <b-row style="flex-direction: column">
      <b-row class="person-info">
        <p class="info-title">Роды занятий: &nbsp;</p>
        <p><b-link class="info-link">Драматург</b-link>, <b-link class="info-link">поэт</b-link></p>
      </b-row>
      <b-row class="person-info">
        <p class="info-title">Постоянная ссылка на данное описание: &nbsp;</p>
        <p class="info-link"><b-link class="info-link" to="persontype">http://theatre-museum.ru/object/2472680</b-link></p>
      </b-row>
    </b-row>
    <content-tabs />
  </b-container>
</template>

<script>
import ContentTabs from "@/components/ContentTabs";
import BreadCrumbs from "@/components/BreadCrumbs";
import PageTitle from "@/components/PageTitle";
export default {
  name: "personType",
  components: {PageTitle, BreadCrumbs, ContentTabs},
  data() {
    return {
      pageTitle: 'Байрон Джордж Гордон',
      breadCrumbItems: [
        {
          text: 'Главная',
          to: '/'
        },
        {
          text: 'Именной указатель',
          to: 'persons'
        },
        {
          text: 'Байрон Джордж Гордон',
          active: 'true'
        }
      ]
    }
  }
}
</script>

<style>
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .main-content {
    padding-left: 15px;
    padding-right: 15px;
  }

  .person-date {
    font-size: 20px;
    line-height: 1.6;
    flex-direction: column;
    margin-bottom: 30px;
  }


  .person-date p {
    margin-bottom: 0;
  }

  .info-title {
    color: #9f959d;
    margin-bottom: 0;
  }

  .info-link {
    font-weight: bold;
    text-decoration: underline;
    margin-bottom: 0;
  }

  .info-link:hover {
    color: #d78d5e !important;
  }

  .person-text {
    margin-bottom: 30px;
    font-size: 18px;
    line-height: 1.778;
    text-align: justify;
  }

  .person-info, .person-info p {
    text-align: left;
    margin: 0 0 5px;
  }
}
@media (min-width: 768px) {

}
/* пк версия более 1024 px*/
@media (min-width: 1024px) {

}
</style>
