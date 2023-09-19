<template>
  <div class="mobileHeader">
    <div class="mobileSearch">
      <button class="goBackButton"></button>
      <input type="text" class="inputSearch" placeholder="Запрос">
      <button class="clearSearch"></button>
      <button class="findButton">Найти</button>
      <hr class="line">
    </div>
  </div>
</template>
<script></script>
<style scoped>
.mobileHeader {
  width: 100%;
  height: 53px;
  padding-top: 8px;
  margin-bottom: 6px;
  position: relative;

  .mobileSearch {
    width: 100%;
    height: 38px;
    display: flex;
    align-items: center;
    justify-content: center;

    .goBackButton {
      display: block;
      min-width: 20px;
      height: 20px;
      background: none;
      border: none;
      background-image: url("../../../images/backButton.png");
      background-size: cover;
    }

    .inputSearch {
      width: 100%;
      height: 100%;
      border: none;
      outline: none;
      font-size: 16px;
      padding-left: 16px;
    }

    .clearSearch {
      display: none;
    }

    .inputSearch:focus+.clearSearch {
      display: block;
      min-width: 17px;
      height: 17px;
      background: none;
      border: none;
      background-image: url("../../../images/clearIcon.png");
      background-size: cover;
      margin-right: 12px;
    }

    .findButton {
      min-width: 75px;
      height: 38px;
      background-color: #7397F5;
      border: 1px solid #7397F5;
      border-radius: 5px;
      color: white;
    }

    .line {
      position: absolute;
      border: none;
      bottom: 0;
      right: 0;
      height: 1px;
      background-color: #D5D5D5;
      width: 89%;
    }

    .inputSearch:focus~.line {
      background-color: #7397F5;
    }
  }
}
</style>
