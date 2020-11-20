<template>
  <b-tabs justified class="person-tabs">
    <b-tab v-for="tab in tabContent" :title="tab.tabCaption + ' (' + tab.tabItems.length + ')'">
      <b-row class="pagination-row">
        <pagination />
      </b-row>
      <b-row class="person-row">
        <b-col cols="6" md="4" xl="3" v-for="item in tab.tabItems" class="person-tab-col">
          <b-card class="person-card">
            <div class="person-card-img-cont">
              <b-card-img :src="item.image" top class="person-card-image">
              </b-card-img>
            </div>
            <b-card-text class="person-card-text first-card"><b-link :to="item.link">{{item.text}}</b-link></b-card-text>
          </b-card>
        </b-col>
      </b-row>
    </b-tab>
  </b-tabs>

</template>

<script>
import Pagination from "@/components/Pagination";
export default {
  name: "ContentTabs",
  components: {Pagination},
  props: {
  },
  data() {
    return {
      tabContent: [
        {tabCaption: "Экспонаты",
          tabItems: [
            {
              text: "Афиша с исполнителями. Москва, Государственный академический театр имени Евг. Вахтангова. \"Пристань\" Брехт Б., Бунин И.А., Достоевский Ф.М., Дюрренматт Ф.Й., Миллер А., Пушкин А.С., Де Филиппо Э. 11,12,13,23,24 ноября 2011 г.\n" +
                "              Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/1.png',
              link: ""
            },
            {
              text: "Афиша с исполнителями. Москва, Московский театр Сатиры. \"Мамаша Кураж и ее дети\" Брехт Б. 17 мая, 5, 10, 13 июня 1972 г.Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/2.png',
              link: ""
            },

            {
              text: "Афиша художественная. Москва, Московский театр драмы и комедии на Таганке. \"Добрый человек из Сезуана\" Брехт Б. 11.03.1969\n" +
                "                    Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/3.png',
              link: ""
            },
            {
              text: "Афиша с исполнителями. Москва, Государственный академический театр имени Евг. Вахтангова. \"Пристань\" Брехт Б., Бунин И.А., Достоевский Ф.М., Дюрренматт Ф.Й., Миллер А., Пушкин А.С., Де Филиппо Э. 11,12,13,23,24 ноября 2011 г.\n" +
                "              Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/1.png',
              link: ""},
            {
              text: "Афиша с исполнителями. Москва, Московский театр Сатиры. \"Мамаша Кураж и ее дети\" Брехт Б. 17 мая, 5, 10, 13 июня 1972 г.Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/2.png',
              link: ""},
            {
              text: "Афиша художественная. Москва, Московский театр драмы и комедии на Таганке. \"Добрый человек из Сезуана\" Брехт Б. 11.03.1969\n" +
                "                    Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/3.png',
              link: ""},
          ]
        },
        {tabCaption: "Театры",
          tabItems: [
            {
              text: "Афиша с исполнителями. Москва, Государственный академический театр имени Евг. Вахтангова. \"Пристань\" Брехт Б., Бунин И.А., Достоевский Ф.М., Дюрренматт Ф.Й., Миллер А., Пушкин А.С., Де Филиппо Э. 11,12,13,23,24 ноября 2011 г.\n" +
                "              Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/1.png',
              link: ""
            },
            {
              text: "Афиша с исполнителями. Москва, Московский театр Сатиры. \"Мамаша Кураж и ее дети\" Брехт Б. 17 мая, 5, 10, 13 июня 1972 г.Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/2.png',
              link: ""
            },

            {
              text: "Афиша художественная. Москва, Московский театр драмы и комедии на Таганке. \"Добрый человек из Сезуана\" Брехт Б. 11.03.1969\n" +
                "                    Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/3.png',
              link: ""
            },
            {
              text: "Афиша с исполнителями. Москва, Государственный академический театр имени Евг. Вахтангова. \"Пристань\" Брехт Б., Бунин И.А., Достоевский Ф.М., Дюрренматт Ф.Й., Миллер А., Пушкин А.С., Де Филиппо Э. 11,12,13,23,24 ноября 2011 г.\n" +
                "              Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/1.png',
              link: ""},
            {
              text: "Афиша с исполнителями. Москва, Московский театр Сатиры. \"Мамаша Кураж и ее дети\" Брехт Б. 17 мая, 5, 10, 13 июня 1972 г.Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/2.png',
              link: ""},
            {
              text: "Афиша художественная. Москва, Московский театр драмы и комедии на Таганке. \"Добрый человек из Сезуана\" Брехт Б. 11.03.1969\n" +
                "                    Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/3.png',
              link: ""},
          ]
        },
        {tabCaption: "Mузеи",
          tabItems: [
            {
              text: "Афиша с исполнителями. Москва, Государственный академический театр имени Евг. Вахтангова. \"Пристань\" Брехт Б., Бунин И.А., Достоевский Ф.М., Дюрренматт Ф.Й., Миллер А., Пушкин А.С., Де Филиппо Э. 11,12,13,23,24 ноября 2011 г.\n" +
                "              Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/1.png',
              link: ""
            },
            {
              text: "Афиша с исполнителями. Москва, Московский театр Сатиры. \"Мамаша Кураж и ее дети\" Брехт Б. 17 мая, 5, 10, 13 июня 1972 г.Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/2.png',
              link: ""
            },

            {
              text: "Афиша художественная. Москва, Московский театр драмы и комедии на Таганке. \"Добрый человек из Сезуана\" Брехт Б. 11.03.1969\n" +
                "                    Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/3.png',
              link: ""
            },
            {
              text: "Афиша с исполнителями. Москва, Государственный академический театр имени Евг. Вахтангова. \"Пристань\" Брехт Б., Бунин И.А., Достоевский Ф.М., Дюрренматт Ф.Й., Миллер А., Пушкин А.С., Де Филиппо Э. 11,12,13,23,24 ноября 2011 г.\n" +
                "              Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/1.png',
              link: ""},
            {
              text: "Афиша с исполнителями. Москва, Московский театр Сатиры. \"Мамаша Кураж и ее дети\" Брехт Б. 17 мая, 5, 10, 13 июня 1972 г.Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/2.png',
              link: ""},
            {
              text: "Афиша художественная. Москва, Московский театр драмы и комедии на Таганке. \"Добрый человек из Сезуана\" Брехт Б. 11.03.1969\n" +
                "                    Государственный центральный театральный музей имени А. А. Бахрушина",
              image:'~assets/img/persons/3.png',
              link: ""},
          ]
        }

      ],
    }
  }


}
</script>

<style>
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .person-tabs {
    margin-left: -15px;
    margin-right: -15px;
  }
  .person-row {
    margin-bottom: 30px;
    padding-left: 15px;
    padding-right: 15px;
  }
  .person-tab-col {
    padding: 0;
  }

  .person-card {
    border: none;
    border-radius: 0;
    padding: 0;
    margin-bottom: 15px;
  }
  .person-card .card-body {
    padding: 0;
    text-align: center;
  }
  .person-card-img-cont {
    background-color: #f5f2ec;
    width: 16vw;
    height: 16vw;
    min-height: 130px;
    min-width: 130px;
    padding: 0;
    display: flex;
    margin: auto;

  }

  .person-card-image {
    object-fit: contain;

  }
  .person-card-text {

    width: 16vw;
    min-width: 130px;
    margin: 15px auto;
    text-align: left;
    max-height: 125px;
    overflow: hidden;
  }
  .person-card-text a{
    font-size: 14px;
    color: #270000 !important;
    font-weight: bold;
    text-decoration: underline;
    line-height: 1.2;
    color: #270000;


  }
  .person-card-text:hover a{
    color: #d78d5e !important;
  }

  .info-link:hover{
    color: #d78d5e !important;
  }
  .person-tabs {
    margin-top: 30px;
  }
  .nav-tabs {
    border: none;
    display: flex;
  }
  .nav-item {
    margin: auto;
    height: 65px;
  }
  .nav-tabs .nav-link {
    background-color: #dfd0b3 !important;
    border: none;
    border-radius: 0;
    padding: 17px 15px;
    font-size: 14px;
    font-weight: bold;
    line-height: 1.2;
    height: 100%;


  }
  .nav-tabs .nav-link.active {
    background-color: #d3c2a2 !important;
    color: #270000;
  }
}
/* планшетная версия - 768-1024 px*/
@media (min-width: 768px) {

}
/* пк версия более 1024 px*/
@media (min-width: 1024px) {
  .person-card-img-cont {
    background-color: #f5f2ec;
    width: 13vw;
    height: 13vw;
    min-height: 130px;
    min-width: 130px;
    padding: 0;
    display: flex;
    margin: auto;

  }

  .person-card-image {
    object-fit: contain;

  }
  .person-card-text {

    width: 13vw;

    margin: 15px auto;
    line-height: 1.6;

    max-height: 180px;

  }
  .person-card-text a {
    font-size: 16px;
  }
  .nav-tabs .nav-link {
    font-size: 16px;
  }
}
</style>
