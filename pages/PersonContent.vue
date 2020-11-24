<template>
  <b-row class="content-row">
    <b-col class="content-info" cols="12" md="8">
      <b-row class="person-date">
        <p>(англ. George Gordon Byron (Noel))</p>
        <p>(22 января 1788 года, Лондон — 19 апреля 1824 года, Миссолунги, Османская Греция)</p>
      </b-row>
      <b-row class="person-text">Английский поэт-романтик. Наряду с Перси Шелли и Джоном Китсом представляет младшее
        поколение британских романтиков. Его альтер-эго Чайльд-Гарольд стал прототипом бесчисленных байронических героев
        в литературе разных стран Европы.
      </b-row>
      <b-row style="flex-direction: column">
        <b-row class="person-info">
          <p class="info-title">Роды занятий: &nbsp;</p>
          <p>
            <b-link class="info-link">Драматург</b-link>
            ,
            <b-link class="info-link">поэт</b-link>
          </p>
        </b-row>
        <b-row class="person-info">
          <p class="info-title">Постоянная ссылка на данное описание: &nbsp;</p>
          <p class="info-link">
            <b-link class="info-link" to="persontype">http://theatre-museum.ru/object/2472680</b-link>
          </p>
        </b-row>
      </b-row>
    </b-col>
    <b-col class="content-photo" cols="12" md="4">
      <b-img v-img src="~/assets/img/persons/1-1.png" class="content-photo-img"></b-img>
    </b-col>
  </b-row>
</template>
<script>
export default {
  name: 'PersonContent'
}
</script>
<style lang="scss">
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  .content-row {
    display: flex;
    flex-direction: column-reverse;
    .content-info {
      padding: 0;
      margin-top: 30px;
      .person-title {
        font-size: 20px;
        font-weight: bold;
        padding: 0;
        margin-bottom: 20px;
      }
      .person-date {
        font-weight: bold;
        flex-direction: column;
        margin-bottom: 20px;
        p {
          margin-bottom: 0;
        }
      }
      .person-text {
        margin-bottom: 20px;
      }
      .person-info {
        text-align: left;
        margin: 0;
        p {
          text-align: left;
          margin: 0;
        }
        .info-title {
          color: #9f959d;
          margin-bottom: 0;
        }
        .info-link {
          font-weight: bold;
          text-decoration: underline;
          margin-bottom: 0;
        }

      }

    }
    .content-photo {
      padding: 0;
      .content-photo-img {
        width: 100%;
      }
    }
  }
}

@media (min-width: 768px) {
  .content-row {
    flex-direction: row;

    .content-info {
      padding: 0;
      margin-top: 0;
    }

    .content-photo {
      padding-left: 15px;
    }
  }
}

/* пк версия более 1024 px*/
@media (min-width: 1024px) {

}
</style>
