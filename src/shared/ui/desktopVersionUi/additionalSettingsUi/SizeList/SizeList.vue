<template>
  <div class="size">

    <div class="brandText">
      <p class="keyword">Размер</p>
    </div>

    <ul class="sizesList">
      <li v-for="size in sizes" class="sizeAttribute"><input type="checkbox" class="checkSize">{{ size }}</li>
    </ul>

  </div>
</template>
<script>
export default {
  data() {
    return {
      sizes: [
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут"
      ]
    }
  }
}
</script>
<style scoped>
.size {
  width: 100%;
  height: 216px;

  .brandText {
    display: flex;
    justify-content: center;
    margin-bottom: 16px;

    .keyword {
      font-weight: 700;
    }
  }

  .sizesList {
    width: 100%;
    height: 180px;
    list-style-type: none;

    .sizeAttribute {
      display: flex;
      align-items: center;
      width: 100%;
      height: 20px;
      font-size: 14px;
      margin-bottom: 12px;

      .checkSize {
        width: 20px;
        height: 20px;
        margin-right: 12px;
      }
    }
  }
}
</style>
