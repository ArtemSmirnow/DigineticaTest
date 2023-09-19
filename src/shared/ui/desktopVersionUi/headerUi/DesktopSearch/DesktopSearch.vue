<template>
  <div class="search">
    <input class="input" type="text" placeholder="Поиск по 100 000 товаров">
    <button class="searchButton">Найти</button>
  </div>
</template>
<script></script>
<style scoped>
.search {
  display: flex;
  align-items: center;
  width: 59%;

  .input {
    border: 1px solid #73AFF4;
    border-radius: 10px;
    outline: none;
    width: 100%;
    height: 48px;
    font-size: 16px;
    line-height: 24px;
    background-image: url("../../../../images/search.png");
    background-repeat: no-repeat;
    background-position: 10px;
    padding-left: 40px;

  }

  .searchButton {
    display: none;
  }

  .input:focus {
    padding-right: 80px;
  }

  .input:focus+.searchButton {
    display: block;
    background-color: #73AFF4;
    width: 70px;
    height: 38px;
    margin-left: -74px;
    border: #73AFF4 1px solid;
    font-weight: 700;
    color: white;
    letter-spacing: 1px;
    border-radius: 10px;
  }
}
</style>
