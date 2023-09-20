<template>
  <div class="search">
    <input class="inputSearch" type="text" placeholder="Поиск по 100 000 товаров">
    <button class="searchButton">Найти</button>
    <button class="clearSearch"></button>
  </div>
</template>
<script></script>
<style scoped>
.search {
  display: flex;
  align-items: center;
  width: 59%;

  .inputSearch {
    border: 1px solid #73AFF4;
    border-radius: 10px;
    outline: none;
    width: 100%;
    height: 48px;
    font-size: 16px;
    background-image: url("../../../../images/search.png");
    background-repeat: no-repeat;
    background-position: 10px;
    padding-left: 40px;
  }

  .clearSearch {
    display: none;
  }

  .inputSearch:focus ~ .clearSearch {
    display: block;
    min-width: 17px;
    height: 17px;
    background: none;
    border: none;
    background-image: url("../../../../images/clearIcon.png");
    background-size: cover;
    margin-left: -95px;
  }

  .searchButton {
    display: none;
  }

  .inputSearch:focus {
    padding-right: 80px;
  }

  .inputSearch:focus~.searchButton {
    display: block;
    background-color: #73AFF4;
    min-width: 70px;
    height: 38px;
    margin-left: -74px;
    border: #73AFF4 1px solid;
    font-weight: 700;
    color: white;
    border-radius: 10px;
  }
}
</style>
