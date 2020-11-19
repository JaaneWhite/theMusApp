<template>
  <b-nav fill class="site-menu">
    <b-nav-item to="/" class="menu-button">
      <b-img src="~assets/img/home.png" class="home-logo" alt="Home"></b-img>
    </b-nav-item>
    <b-nav-item to="/" class="menu-button">Театральные музеи и архивы</b-nav-item>
    <b-nav-item to="/" class="menu-button">Театры</b-nav-item>
    <b-nav-item to="persons" class="menu-button">Именной указатель</b-nav-item>
    <b-nav-item to="/" class="menu-button">Географический указатель</b-nav-item>
  </b-nav>
</template>

<script>
export default {
  name: "TopMenu"
}
</script>

<style scoped>
.site-menu {
  flex-wrap: nowrap;
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


</style>
