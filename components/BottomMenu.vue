<template>
  <div>

    <b-nav class="site-menu menu-lg" fill>

      <b-nav-item to="/" class="menu-button">О&nbsp;ПРОЕКТЕ</b-nav-item>
      <b-nav-item to="/" class="menu-button">АВТОРЫ</b-nav-item>
      <b-nav-item to="/" class="menu-button">УЧАСТНИКИ</b-nav-item>
      <b-nav-item to="/" class="menu-button">ПАРТНЕРЫ</b-nav-item>
      <b-nav-item to="/" class="menu-button">МУЗЕЙНОЕ ЗАКОНОДАТЕЛЬСТВО</b-nav-item>
      <b-nav-item to="/" class="menu-button">КОНТАКТЫ</b-nav-item>

    </b-nav>

    <b-row class="menu-sm">
      <b-col class="menu-sm-col">
        <b-button to="/" class="menu-button">О&nbsp;проекте</b-button>
      </b-col>
      <b-col class="menu-sm-col">
        <b-button to="/" class="menu-button">Партнеры</b-button>
      </b-col>
    </b-row>
    <b-row class="menu-sm">
      <b-col class="menu-sm-col">
        <b-button to="/" class="menu-button">Авторы</b-button>
      </b-col>
      <b-col class="menu-sm-col">
        <b-button to="/" class="menu-button">Музейное <br> законодательство</b-button>
      </b-col>
    </b-row>
    <b-row class="menu-sm">
      <b-col class="menu-sm-col">
        <b-button to="/" class="menu-button">Участники</b-button>
      </b-col>
      <b-col class="menu-sm-col">
        <b-button to="/" class="menu-button">Контакты</b-button>
      </b-col>
    </b-row>

  </div>
</template>

<script>
export default {
  name: "BottomMenu"
}
</script>

<style scoped>
/* мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .menu-lg {
    display: none;
  }
  .menu-sm {
    margin: 0;
  }
  .menu-sm-col {
    height: 50px;
    display: flex;
    padding: 0;

  }
  .menu-sm-col {
    width: 100%;
    margin: auto;
    padding: 0;
    align-items: center;
    display: grid;
    border: solid white 1px;
    text-transform: none;
  }
  .menu-sm-col a {
    color: #270000;
    font-size: 12px;
    font-weight: bold;
    white-space: normal;
    text-align: center;
    display: grid;
    margin: auto;
    border: none;
    border-radius: 0;
    background-color: #e5d1b3;
    width: 100%;
    height: 100%;

  }

}
/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {
  .menu-sm {
    display: none;
  }

  .menu-lg {
    display: flex;
  }
  .site-menu {
    flex-wrap: nowrap;
    background-color: #e5d1b3;
  }
  .menu-button {
    border: none;
    border-radius: 0;
    box-shadow: none;
    height: 60px;
    padding: 0;
    display: flex;
    text-align: center;
    align-items: center;

  }
  .menu-button:hover {
    background-color: #d3c2a2;
  }
  .menu-button a {
    color: #270000;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 14px;
    font-weight: bold;
    white-space: normal;
    text-align: center;
    display: flex;
    margin: auto;
  }
}
/* пк версия - 1024 - ... px*/
@media (min-width: 1024px) {

}
</style>
