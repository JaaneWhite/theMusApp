<template>
  <div>
    <header-component />
    <Nuxt />
    <footer-component />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,300&display=swap');
@media (min-width: 1500px) {
  .container {
    max-width: 1460px;
  }
}

/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  body {
    margin: auto;
    font-family: 'Roboto', sans-serif;
    color: #270000;
  }
  .row, .container {
    padding: 0;
  }
  .row {
    margin: 0;
  }

  a, a:hover{
    color: #270000;
  }


  .sr-only {
    display: none;
  }

  .dropdown-toggle::after {
    content: none;
  }

  .toggle-menu-text-collapse, .toggle-menu-text-collapse:active, .toggle-menu-text-collapse:hover, .toggle-menu-text-collapse:focus, .toggle-menu-text-shown {
    background-color: transparent;
    color: white;
    font-size: 10px;
    text-align: left;
    border: none;
    box-shadow: none;
    width: 75%;
    border-radius: 0;
  }

  .toggle-menu-text-shown, .toggle-menu-text-shown:hover, .toggle-menu-text-shown:active, .toggle-menu-text-shown:focus {
    background-color: #e5d1b3;
    color: #270000;
  }

  .toggle-menu-button-collapse, .toggle-menu-button-collapse:hover, .toggle-menu-button-collapse:focus, .toggle-menu-button-collapse:active, .toggle-menu-button-shown {
    width: 25%;
    background-image: url("~assets/img/menu-icon.png");
    background-repeat: no-repeat;
    background-position: center;
    background-color: transparent;
    padding: 0;
    border: none;
    box-shadow: none;
    border-radius: 0;
  }

  .toggle-menu-button-shown {
    background-color: #e5d1b3;
    background-image: url("~assets/img/menu close.png");
  }

  .show > .btn-secondary.dropdown-toggle {
    background-color: #e5d1b3;
    border: none;
    box-shadow: none;
  }

  .dropdown-menu {
    border-radius: 0;
    border: none;
    background-color: #e5d1b3;
    margin: 0;
    width: 100%;
    transform: translate3d(0, 80px, 0) !important;
    height: 349px;
  }

  .toggle-menu-item a {
    font-size: 16px;
    color: #270000;
    font-weight: bold;
  }

  .list-button, .list-button:hover, .list-button:active, .list-button:focus {
    background-color: white;
    width: 90%;
    color: #270000;
    font-weight: bold;
    text-align: left;
    border-radius: 0;
    border: none;
    box-shadow: none;
  }
  .list-button-dd, .list-button-dd:hover, .list-button-dd:active, .list-button-dd:focus {
    background-color: white;
    background-image: url("~assets/img/list-arrows.png");
    background-repeat: no-repeat;
    background-position: center;
    width: 10%;
    border-radius: 0;
    border: none;
    box-shadow: none;
  }
  .collection-Menu-dd.show > .btn-secondary.dropdown-toggle {
    background-color: white;
    border-radius: 0;
    border: none;
    box-shadow: none;
  }
  .collection-menu-button {
    width: 100%;
    color: #270000;
    font-size: 15px;
    border-bottom: solid #e5eff1 1px;
  }
  .collection-menu-button .dropdown-item {
    color: #270000;
    font-size: 15px;
  }

  .collection-Menu-dd .dropdown-menu {
    width: 100%;
    border-radius: 0;
    border: solid #cf6a40 3px;
    max-height: 560px;
    height: auto;
    overflow: scroll;
    background-color: white;
    color: #270000;
    transform: translate3d(0, 30px, 0) !important;
  }
}
@media (max-width: 1023px) {
  .container {
    max-width: 1023px;
  }
}


</style>
<script>
import HeaderComponent from "~/components/HeaderComponent";
import FooterComponent from "@/components/FooterComponent";
export default {
  components: {FooterComponent, HeaderComponent}
}
</script>
