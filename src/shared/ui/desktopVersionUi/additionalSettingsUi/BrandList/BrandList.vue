<template>
  <div class="brand">
    <div class="brandText">
      <p class="keyword">Бренд</p>
      <button class="clearBtn">Очистить</button>
    </div>
    <div class="searchBrand">
      <input class="inputBrand" type="text" placeholder="Поиск">
      <button class="clearSearch" />
    </div>
    <ul class="attributesList">
      <li v-for="attribute in attributes" class="attribute"><input type="checkbox" class="checkAttribute">{{ attribute }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      attributes: [
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
        "Атрибут",
      ],
    }
  }
}
</script>
<style scoped>
.brand {
  width: 280px;
  height: 268px;
  margin-bottom: 28px;

  .brandText {
    display: flex;
    justify-content: space-between;
    margin-bottom: 16px;

  }

  .keyword {
    font-weight: 700;
  }

  .clearBtn {
    background: none;
    border: none;
    cursor: pointer;
    text-decoration: underline;
    font-size: 12px;
    color: #AAAAAA;
  }
}

.searchBrand {
  display: flex;
  width: 100%;
  height: 36px;
  margin-bottom: 16px;

  .inputBrand {
    border: 1px solid #D5D5D5;
    border-radius: 5px;
    outline: none;
    width: 100%;
    height: 36px;
    margin-bottom: 16px;
    font-size: 14px;
    background-image: url("../../../../images/MobileSearchIcon.png");
    background-repeat: no-repeat;
    background-position: 12px;
    padding-left: 36px;
  }

  .inputBrand:hover {
    border: 1px solid #E2EFFF;
  }

  .inputBrand:focus {
    padding-right: 30px;
    border: 1px solid #7397F5;
  }

  .clearSearch {
    display: none;
  }

  .inputBrand:focus+.clearSearch {
    display: block;
    width: 20px;
    height: 20px;
    align-self: center;
    background: none;
    border: none;
    cursor: pointer;
    background-image: url("../../../../images/clearIcon.png");
    background-size: cover;
    margin-left: -28px;
  }
}

.attributesList {
  width: 100%;
  height: 180px;
  list-style-type: none;
  overflow-y: scroll;

  .attribute {
    display: flex;
    align-items: center;
    width: 100%;
    height: 20px;
    font-size: 14px;
    margin-bottom: 12px;

    .checkAttribute {
      width: 20px;
      height: 20px;
      margin-right: 12px;
    }
  }

}

::-webkit-scrollbar {
  width: 3px;
}

::-webkit-scrollbar-thumb {
  background: #CBCBCB;
}
</style>
