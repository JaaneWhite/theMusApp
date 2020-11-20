<template>
  <b-pagination
    v-model="currentPage"
    :total-rows="totalRows"
    :per-page="perPage"
    :aria-controls="paginationAreaControls"
    pills
    first-number
    last-number
    class="pagination"
    next-text=""
    next-class="pagination-next-button"
    prev-text=""
    prev-class="pagination-prev-button"
  ></b-pagination>
</template>

<script>
export default {
  name: 'pagination',
  data() {
    return {
      currentPage: 1
    }
  },
  props: {
    totalRows: {},
    paginationAreaControls: {},
    perPage: {}
  }
}
</script>

<style>
.pagination {
  margin: 30px auto;
}
.page-item.disabled .page-link, .page-item .page-link, .page-item:hover .page-link {
  color: #270000;
  background-color: transparent;
  font-size: 14px;
  line-height: 1.2 !important;
  box-shadow: none;
  border: none;
}
.page-item.active .page-link {
  color: #270000;
  background-color: #f1eae0;
  border: none;
  font-size: 14px;
  line-height: 1.2;
  box-shadow: none;
}
.pagination-next-button {
  background-image: url("~assets/img/arrow right.png");
  background-repeat: no-repeat;
  background-position: center;
}
.pagination-prev-button {
  background-image: url("~assets/img/arrow left.png");
  background-repeat: no-repeat;
  background-position: center;
}
</style>
