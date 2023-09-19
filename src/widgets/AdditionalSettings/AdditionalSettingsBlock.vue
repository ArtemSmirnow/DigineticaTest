<template>
  <div class="settings">
    <CategoryList />
    <PriceRange />
    <BrandList />
    <SizeList />
  </div>
</template>
<script>
import CategoryList from "../../shared/ui/desktopVersionUi/additionalSettingsUi/CategoryList/CategoryList.vue";
import PriceRange from "../../shared/ui/desktopVersionUi/additionalSettingsUi/PriceRange/PriceRange.vue";
import BrandList from "../../shared/ui/desktopVersionUi/additionalSettingsUi/BrandList/BrandList.vue";
import SizeList from "../../shared/ui/desktopVersionUi/additionalSettingsUi/SizeList/SizeList.vue";
export default {
  components: {
    CategoryList,
    PriceRange,
    BrandList,
    SizeList
  }
}
</script>
<style scoped>
.settings {
  align-self: flex-start;
  width: 280px;
  height: 760px;
  margin-top: 24px;
}

input[type=checkbox]:hover {
  cursor: pointer;
}
</style>
