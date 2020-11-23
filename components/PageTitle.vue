<template>
  <b-row class="page-title">{{pageTitleText}}</b-row>
</template>

<script>
export default {
  name: 'pageTitle',
  props: {
    pageTitleText: {}
  }
}
</script>

<style scoped>
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .page-title {
    font-size: 24px;
    margin-bottom: 25px;
    margin-top: 24px;
    font-weight: bold;
    line-height: 1.389;
  }
}
/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {
  .page-title {
    font-size: 24px;
  }
}
/* пк версия более 1024 px*/
@media (min-width: 1024px) {
  .page-title {
    font-size: 36px;
  }
}

</style>
