<template>
  <b-form-group class="alphabet-group">
    <b-form-radio-group
        id="btn-radios-1"
        v-model="alphabetSelected"
        :options="alphabetOptions"
        buttons
        name="radios-btn-default"
        @change="onSelectChanges()"
    ></b-form-radio-group>
  </b-form-group>
</template>
<script>
export default {
  name: 'AlphabetSort',

  data () {
    return {
      alphabetSelected: 'А',
      alphabetOptions: [
        { text: 'А', value: 'А' },
        { text: 'Б', value: 'Б' },
        { text: 'В', value: 'В' },
        { text: 'Г', value: 'Г' },
        { text: 'Д', value: 'Д' },
        { text: 'Е', value: 'Е' },
        { text: 'Ё', value: 'Ё' },
        { text: 'Ж', value: 'Ж' },
        { text: 'З', value: 'З' },
        { text: 'И', value: 'И' },
        { text: 'Й', value: 'Й' },
        { text: 'К', value: 'К' },
        { text: 'Л', value: 'Л' },
        { text: 'М', value: 'М' },
        { text: 'Н', value: 'Н' },
        { text: 'О', value: 'О' },
        { text: 'П', value: 'П' },
        { text: 'Р', value: 'Р' },
        { text: 'С', value: 'С' },
        { text: 'т', value: 'Т' },
        { text: 'У', value: 'У' },
        { text: 'Ф', value: 'Ф' },
        { text: 'Х', value: 'Х' },
        { text: 'Ц', value: 'Ц' },
        { text: 'Ч', value: 'Ч' },
        { text: 'Ш', value: 'Ш' },
        { text: 'Щ', value: 'Щ' },
        { text: 'Э', value: 'Э' },
        { text: 'Ю', value: 'Ю' },
        { text: 'Я', value: 'Я' }
      ]
    }
  },
  methods: {
    onSelectChanges: function () {
      this.$emit("selectChanged", this.alphabetSelected)
    }
  }
}
</script>
<style lang="scss">
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .alphabet-group {
    .btn-group {
      display: block;
    }
    .btn-secondary{
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
      &:hover {
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
      &.active {
        background-color: #eeeadf !important;
        color: #270000 !important;
        box-shadow: none;
      }
    }
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
