<template>
  <b-row class="toggle-menu-row">
    <b-dropdown class="toggle-menu"
                split
                :split-class="toggleMenuSplitClass"
                :toggle-class="toggleMenuButtonClass"
                v-on:shown="toggleMenuSplitClass='toggle-menu-text-shown'; toggleMenuButtonClass='toggle-menu-button-shown'"
                v-on:hidden="toggleMenuSplitClass='toggle-menu-text-collapse'; toggleMenuButtonClass='toggle-menu-button-collapse'"
                :text="toggleMenuText"

    >

        <b-dropdown-item class="toggle-menu-item" v-for="menuItem in menuItems" :to=menuItem.link>{{menuItem.text}}</b-dropdown-item>


    </b-dropdown>
  </b-row>

</template>
<script>
export default {
  name: 'ToggleMenu',
  data() {
    return {
      toggleMenuSplitClass: 'toggle-menu-text-collapse',
      toggleMenuButtonClass: 'toggle-menu-button-collapse',
      toggleMenuText: "Портал создан на средства гранта Президента\n" +
        "      Российской Федерации для поддержки\n" +
        "      творческих проектов общенационального\n" +
        "      значения в области культуры и искусства",
      menuItems: [
        {text: 'Главная', link: '/'},
        {text: 'Театральные музеи и архивы', link: '/'},
        {text: 'Театры', link: '/'},
        {text: 'Именной указатель', link: 'persons'},
        {text: 'Географический указатель', link: '/'},
      ]

    }
  }
}
</script>
<style scoped>
.toggle-menu-row {
  width: 100%;
  margin-left: 0;
  margin-right: 0;
}
.toggle-menu {
  width: 100%;
  height: 80px;
  font-size: 10px;

}
.toggle-menu-item {
  height: 50px;
  border-bottom: solid #d3c2a2 1px;
  display: flex;
  align-items: center;
}

</style>
