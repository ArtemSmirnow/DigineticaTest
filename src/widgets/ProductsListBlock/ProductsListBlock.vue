<template>
  <div class="productsListBlock">
    <ProductsList />
  </div>
</template>
<script>
import ProductsList from "../../shared/ui/desktopVersionUi/productsListUi/ProductsList.vue"
export default {
  components: {
    ProductsList
  }
}
</script>
<style scoped>
.productsListBlock {
  margin-top: 24px;
  margin-left: 36px;
  width: 1404px;
}
</style>
