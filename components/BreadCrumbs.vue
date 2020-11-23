<template>
  <b-breadcrumb :items="breadCrumbItems"></b-breadcrumb>
</template>

<script>
export default {
  name: 'breadCrumbs',
  props: {
    breadCrumbItems: {}
  }
}
</script>

<style scoped>
.breadcrumb {
  background-color: transparent;
  color: #cac3b1;
  padding: 0;
}
.breadcrumb-item a, .breadcrumb-item.active {
  color: #cac3b1 !important;
}
.breadcrumb-item a {
  text-decoration: underline;
}
.breadcrumb-item {
  font-size: 14px;
}

</style>
