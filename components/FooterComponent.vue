<template>
  <footer>
    <b-row class="menu-row">
      <b-container class="menu-row-container bottom-menu">
        <bottom-menu />
      </b-container>
    </b-row>
    <b-container class="footer-links">
      <b-row class="footer-links-1">
        <b-col cols="12" md="4" xl="2" class="footer-link">
          <b-link href="">Программа грантов Президента РФ в области культуры и искусства</b-link>
        </b-col>
        <b-col cols="0" xl="4" class="footer-text f-t-1">
          <b-row>&copy Государственный центральный театральный музей имени А.А. Бахрушина</b-row>
          <b-row>&copy АЛЬТ-СОФТ</b-row>
        </b-col>
        <b-col cols="4" md="2" xl="2" class="footer-img">
          <b-img src="~assets/img/footer/minkult.png"></b-img>
        </b-col>
        <b-col cols="4" md="3" xl="2" class="footer-img">
          <b-img src="~assets/img/footer/bahr.png"></b-img>
        </b-col>
        <b-col cols="4" md="3" xl="2" class="footer-img">
          <b-img src="~assets/img/footer/altsoft.png"></b-img>
        </b-col>
      </b-row>
      <b-row class="footer-text f-t-2">&copy Государственный центральный театральный музей имени А.А. Бахрушина</b-row>
      <b-row class="footer-text f-t-2">&copy АЛЬТ-СОФТ</b-row>
    </b-container>
  </footer>
</template>

<script>
import BottomMenu from "@/components/BottomMenu";
export default {
  name: "FooterComponent",
  components: {BottomMenu}
}
</script>

<style scoped>
/* мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .footer-links {
    margin-bottom: 30px;
    padding-left: 15px;
    padding-right: 15px;
  }
  .f-t-1 {
    display: none;
  }
  .f-t-2 {
    display: block;
    text-align: center;

  }
  .footer-img {
    height: 80px;
    display: grid;
    align-items: center;
    padding: 3px;
  }
  .footer-img img {
    margin: auto;
    max-width: 100%;
  }
  .footer-links-1 {
    margin-top: 30px;
    padding-bottom: 30px;
    margin-bottom: 30px;
    border-bottom: solid #d3c2a2 1px;

  }
  .footer-link {
    display: flex;
    margin-bottom: 30px;
  }
  .footer-link a{
    text-decoration: underline;
    color: #270000;
    text-align: center;
    margin: auto;
    font-weight: bold;
    font-size: 14px;
    line-height: 1.571;
  }
  .footer-text {
    font-size: 14px;
    line-height: 1.714;
  }
  .menu-row {
    background-color: white;
  }
}
/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {
  .footer-link {
    margin-bottom: 0;
  }
  .footer-link a{
    text-align: left;
  }
  .menu-row {
    background-color: #e5d1b3;
  }

}
/* пк версия - 1024 - ... px*/
@media (min-width: 1024px) {
  .f-t-1 {
    display: flex;
    flex-direction: column;
  }
  .f-t-2 {
    display: none;
  }
  .footer-links-1 {
    border: none;
  }
  .footer-links {
    margin-bottom: 0;
  }
  .footer-text {
    line-height: 1.85
  }

}
</style>
