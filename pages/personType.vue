<template>
  <b-container class="main-content">
    <b-row class="breadcrumb-row">
      <bread-crumbs :bread-crumb-items="breadCrumbItems"/>

    </b-row>
    <page-title :page-title-text="pageTitle"/>
    <PersonContent/>
    <content-tabs cards-row-size="3" />
  </b-container>
</template>

<script>
import ContentTabs from "@/components/ContentTabs";
import BreadCrumbs from "@/components/BreadCrumbs";
import PageTitle from "@/components/PageTitle";
import PersonContent from "@/pages/PersonContent";

export default {
  name: "personType",
  components: {PersonContent, PageTitle, BreadCrumbs, ContentTabs},
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

<style lang="scss" scoped>
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .main-content {
    padding-left: 15px;
    padding-right: 15px;
  }
}
@media (min-width: 768px) {
  .content-col {
    padding-left: 20px;
    margin-top: 0;
  }
}
/* пк версия более 1024 px*/
@media (min-width: 1024px) {

}
</style>
