<template>
  <MobileHeader />
  <MobileProductsList />
</template>
<script>
import MobileHeader from "../../shared/ui/mobileVersionUi/MobileHeader/MobileHeader.vue";
import MobileProductsList from "../../shared/ui/mobileVersionUi/MobileProductsList/MobileProductsList.vue";
export default {
  components: {
    MobileHeader,
    MobileProductsList
  }
}
</script>
<style>
</style>
