<template>
  <b-nav vertical class="collection-menu" :items="menuListItems">


    <b-nav-item class="c-menu-button" v-for="menuItem in menuListItems">{{menuItem.text}}</b-nav-item>

  </b-nav>
</template>
<script>
export default {
  name: 'MenuList',
  props: {
    menuListItems: {},
  }
}
</script>
<style lang="scss" scoped>
.c-menu-button {
  margin: 0;
  padding-bottom: 6px;
  height: auto;
  a {
    padding-left: 0;
    color: #270000;
    font-size: 16px;
    line-height: 1.45;
    &:hover {
      color: #d78d5e !important;
    }
  }
}


</style>
