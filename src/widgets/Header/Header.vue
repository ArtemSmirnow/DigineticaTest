<template>
  <div class="header">
    <Logo />
    <Catalog />
    <Search />
    <LinksList />
  </div>
</template>
<script>
import Logo from '../../shared/ui/desktopVersionUi/headerUi/Logo/Logo.vue';
import Catalog from '../../shared/ui/desktopVersionUi/headerUi/Catalog/Catalog.vue';
import Search from '../../shared/ui/desktopVersionUi/headerUi/DesktopSearch/DesktopSearch.vue';
import LinksList from '../../shared/ui/desktopVersionUi/headerUi/LinksList/LinksList.vue';
export default {
  components: {
    Logo,
    Catalog,
    Search,
    LinksList
  }
}  
</script>
<style scoped>
.header {
  width: 1720px;
  padding: 12px 0;
  display: flex;
  align-items: center;
}
</style>
