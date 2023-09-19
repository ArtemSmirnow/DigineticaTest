<template>
  <div class="category">
    <input type="checkbox" id="mainCategory" class="mainCategory">
    <label for="mainCategory" class="mainCategoryLabel">Название категории</label>

    <input type="checkbox" id="first" class="subCategory">
    <label for="first" class="subCategoryLabel" id="firstLabel">Название категории</label>

    <input type="checkbox" id="second" class="subCategory">
    <label for="second" class="subCategoryLabel" id="secondLabel">Название категории</label>

    <input type="checkbox" id="third" class="subCategory">
    <label for="third" class="subCategoryLabel" id="thirdLabel">Название категории</label>
  </div>
</template>
<script></script>
<style scoped>
.category {
  width: 280px;

  .mainCategory {
    height: 30px;
    padding-left: 8px;
  }

  .mainCategoryLabel {
    display: flex;
    align-items: center;
    height: 30px;
    width: 100%;
    padding-left: 8px;
  }
}

.subCategoryLabel {
  list-style-type: none;
  display: none;
}

.mainCategory:checked~.subCategoryLabel {
  color: black;
  display: flex;
  align-items: center;
  width: 100%;
  padding-left: 32px;
  height: 30px;
}

.mainCategoryLabel:hover {
  color: #7397F5;
}

#firstLabel:hover {
  color: #7397F5;
}

#secondLabel:hover {
  color: #7397F5;
}

#thirdLabel:hover {
  color: #7397F5;
}

#first:checked~#firstLabel {
  background-color: #E2EFFF;
  border: 1px solid #E2EFFF transparent;
  border-radius: 5px;
}

#second:checked~#secondLabel {
  background-color: #E2EFFF;
  border: 1px solid #E2EFFF transparent;
  border-radius: 5px;
}

#third:checked~#thirdLabel {
  background-color: #E2EFFF;
  border: 1px solid #E2EFFF transparent;
  border-radius: 5px;
}

input[type="checkbox"] {
  display: none;
}
</style>
