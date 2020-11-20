<template>
  <b-form-group class="alphabet-group">
    <b-form-radio-group
        id="btn-radios-1"
        v-model="alphabetSelected"
        :options="alphabetOptions"
        buttons
        name="radios-btn-default"
    ></b-form-radio-group>
  </b-form-group>
</template>
<script>
export default {
  name: 'AlphabetSort',
  props: {
    alphabetOptions: {},
    alphabetSelected: {}
  }
}
</script>
<style>
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .alphabet-group .btn-group {
    display: block;
  }

  .alphabet-group .btn-secondary,.alphabet-group .btn-secondary:hover  {
    background-color: white;
    color: #270000;
    font-size: 16px;
    font-weight: bold;
    text-transform: uppercase;
    line-height: 1.5;
    border: none;
    border-radius: 25px !important;
    height: 34px;
    width: 34px;
    margin: 5px !important;
    box-shadow: none;
  }
  .alphabet-group .btn-secondary.active {
    background-color: #eeeadf !important;
    color: #270000 !important;
    box-shadow: none;
  }
}

/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {
  .alphabet-group {
    display: none;
  }
}

/* пк версия более 1024 px*/
@media (min-width: 1024px) {

}
</style>
