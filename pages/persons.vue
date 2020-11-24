<template>
  <b-container class="main-content">
    <b-row class="breadcrumb-row">
      <bread-crumbs :bread-crumb-items="breadCrumbItems" />
    </b-row>
    <page-title :page-title-text="pageTitleText" />
    <b-row>
      <b-col cols="12" md="3"
             class="menu-col"
      >

        <AlphabetSort
          class="alphabet-sort"
          v-on:selectChanged="alphabetSelectChanged"
        />

        <b-button v-b-modal.modalPopover class="person-select-button">{{selectedPerson}}</b-button>

        <b-modal id="modalPopover"  hide-footer>
          <template #modal-header="{ close }">
            <!-- Emulate built in modal header close button action -->
              <div class="modal-header-title">
                {{'Персоны - ' + pAlphabetSelected}}
              </div>
              <b-col class="modal-header-btn-block">
                <b-button @click="close()" class="modal-close-button">
                </b-button>
              </b-col>
          </template>
          <b-list-group class="person-list-group">
            <b-list-group-item
              v-for="listItem in personlist"
              @click="selectedPerson = listItem.text; $bvModal.hide('modalPopover')"
              class="person-list-item"
            >
              {{listItem.text}}
            </b-list-group-item>
          </b-list-group>

        </b-modal>

        <b-row class="left-pagination-row">
          <pagination
            class="person-list-pagination"
            :total-rows="personNameListRows"
            :pagination-area-controls="personListPaginationAreaControls"
            :per-page="personNameListPerPage"/>
        </b-row>
        <menu-list
          :menu-list-items="personlist"
          id="person-name-list"
          class="menu-list"
        />
        <b-row class="left-pagination-row">
          <pagination
            class="person-list-pagination"
            :total-rows="personNameListRows"
            :pagination-area-controls="personListPaginationAreaControls"
            :per-page="personNameListPerPage"/>
        </b-row>

      </b-col>
      <b-col cols="12" md="9" class="content-col">
        <b-row class="person-title">{{personTitle}}</b-row>
        <person-content />
        <ContentTabs cards-row-size="4" />
      </b-col>
    </b-row>

  </b-container>
</template>

<script>
import Pagination from "@/components/Pagination";
import MenuList from "@/components/MenuList";
import AlphabetSort from "@/components/AlphabetSort";
import ContentTabs from "@/components/ContentTabs";
import BreadCrumbs from "@/components/BreadCrumbs";
import PageTitle from "@/components/PageTitle";
import Vue from 'vue';
import VueImg from 'v-img';
import PersonContent from "@/pages/PersonContent";
Vue.use(VueImg);
export default {
  name: "persons",
  components: {PersonContent, PageTitle, BreadCrumbs, ContentTabs, AlphabetSort, MenuList, Pagination},
  data() {
    return {
      pageTitleText: 'Персоны',
      personTitle: 'Байрон Джордж Гордон',
      personListPaginationAreaControls: 'person-name-list',
      personNameListPerPage: '20',
      selectedPerson: 'Персоны',
      breadCrumbItems: [
        {
          text: 'Главная',
          to: '/'
        },
        {
          text: 'Именной указатель',
          active: true
        }
      ],
      personlist: [
        {text: 'Абади Мартин', link: 'persons'},
        {text: 'Абадиев Бек', link: 'persons'},
        {text: 'Абакаров Ахмедхан', link: 'persons'},
        {text: 'Абасов Магомед Абасович (Абасил)', link: 'persons'},
        {text: 'Абашеев Петр Тимофеевич', link: 'persons'},
        {text: 'Абашова Мария Юрьевна', link: 'persons'},
        {text: 'Аббасов Азат Зиннатович', link: 'persons'},
        {text: 'Абдиев Султан Назирович', link: 'persons'},
        {text: 'Абдоков Маталио Умарович', link: 'persons'},
        {text: 'Абдулгапуров Хайбула Абдулович', link: 'persons'},
        {text: 'Абдуллаев Кемал Джан-Бахиш оглы', link: 'persons'},
        {text: 'Абдуллаев Шахмардан Гасан-Гусейнович', link: 'persons'},
        {text: 'Абдуллин Азат Хамматович', link: 'persons'},
        {text: 'Абдулмуслимова Сапият', link: 'persons'},
        {text: 'Абдулов Александр', link: 'persons'},
        {text: 'Абдулов Гавриил Данилович', link: 'persons'},
        {text: 'Абдулхак Хамид Тархан', link: 'persons'},
        {text: 'Абдулхаликов Махмуд Абдулхаликович', link: 'persons'},
        {text: 'Абдураззаков Барзу', link: 'persons'},
        {text: 'Абелева-Таганова Нателла Матвеевна', link: 'persons'},
        {text: 'Абэ, Кобо', link: 'persons'},
        {text: 'Авалиани Ной Иванович', link: 'persons'},
        {text: 'Аверин Андрей Викторович', link: 'persons'},
      ],
      pAlphabetSelected: 'A'
    }
  },
  computed: {
    personNameListRows() {
      return this.personlist.length
    }
  },
  methods: {
    alphabetSelectChanged: function (alphabetSelected){
      this.pAlphabetSelected = alphabetSelected;
    }
  }
}

</script>

<style lang="scss">
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .main-content {
    padding-left: 15px;
    padding-right: 15px;
  }
  .content-col {
    padding: 0;
    margin-top: 30px;
    .person-title {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 30px;
    }
  }
  .menu-list, .person-list-pagination {
    display: none;
  }
  .menu-col {
    padding: 0;
  }

  .person-select{
    &-button, &-button:hover, &-button:focus, &-button:active{
      border: solid #cf6a40 3px;
      width: 100%;
      border-radius: 0;
      background-color: white;
      color: #270000;
      box-shadow: none;
      height: 40px;
      overflow: hidden;
      padding-right: 15%;
      text-align: left;
      font-weight: bold;
      font-size: 14px;
      background-image: url("~assets/img/list-arrows.png");
      background-repeat: no-repeat;
      background-position-y: center;
      background-position-x: 95%;
    }
  }
  .modal-content {
    border-radius: 0;
    border: solid #cf6a40 3px;
    .modal-header {
      .modal-header-title {
        width: 80%;
        display: flex;
        font-size: 26px;
        font-family: 'Roboto', sans-serif;
        align-items: center;
        color: #270000;
        padding-top: 5px;
      }
      .modal-header-btn-block {
        width: 20%;
        .modal-close-button, .modal-close-button:hover, .modal-close-button:active, .modal-close-button:focus {
          background-image: url("~assets/img/menu close.png");
          background-repeat: no-repeat;
          background-position-x: right;
          background-position-y: center;
          background-color: white;
          width: 50px;
          height: 50px;
          border: none;
          border-radius: 0;
          margin-right: 0;
        }
      }
    }
    .modal-body {
      .person-list-group {
        border: none;
        border-radius: 0;
        overflow: scroll;
        height: 600px;
        .person-list-item {
          border: none;
          border-bottom: solid #9f959d 1px;
        }
      }
    }
  }
}
/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {

  .menu-list, .person-list-pagination {
    display: flex;
  }
  .person-select-button {
    display: none;
  }
  .person-list-pagination {
    text-align: center;
    margin: auto;
  }
  .left-pagination-row {
    padding-top: 10px;
    padding-bottom: 30px;
  }
  .content-col {
    padding: 0;
    margin-top: 0;
    .person-title {
      font-size: 24px;

    }
  }
}



/* пк версия более 1024 px*/
@media (min-width: 1024px) {
  .content-col {
    padding-left: 40px;
    .person-title {
      font-size: 26px;
      margin-bottom: 20px;
    }
    .person-text {
      margin-bottom: 20px;
    }
  }
}
</style>
