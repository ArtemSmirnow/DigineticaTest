<template>
  <!-- Пока не смог найти как динамично добавлять символ рубля в конце -->
  <div class="price">
    <p class="priceText">Цена</p>
    <div class="priceRange">
      <input type="number" placeholder="от" class="range" min="0">
      <span>&mdash;</span>
      <input type="text" placeholder="до" class="range">
    </div>
  </div>
</template>
<script></script>
<style scoped>
.price {
  width: 280px;
  height: 72px;
  margin-top: 28px;
  margin-bottom: 28px;

  .priceText {
    font-weight: 700;
    display: flex;
    justify-content: center;
  }
}



.priceRange {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 16px;
  color: #D5D5D5;

  .range {
    width: 119px;
    height: 36px;
    padding-left: 5px;
    border: 1px solid #D5D5D5;
    border-radius: 5px;
  }

  .range:hover {
    border: 1px solid #E2EFFF;
  }

  .range:focus {
    outline: none;
    border: 1px solid #7397F5;
  }

  .range::placeholder {
    color: #D5D5D5;
    font-family: 'Inter', sans-serif;
    font-size: 12px;
  }
}

input::-webkit-inner-spin-button {
  -webkit-appearance: none;
}
</style>
