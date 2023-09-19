<template>
  <div class="app">
    <div class="desktopPage">
      <div class="head">
        <Header />
      </div>
      <div class="main">
        <AdditionalSettingsBlock />
        <ProductsListBlock />
      </div>
    </div>
    <div class="mobilePage">
      <MobilePage />
    </div>
  </div>
</template>
<script>
import Header from "../widgets/Header/Header.vue";
import AdditionalSettingsBlock from "../widgets/AdditionalSettings/AdditionalSettingsBlock.vue";
import ProductsListBlock from "../widgets/ProductsListBlock/ProductsListBlock.vue";
import MobilePage from "../widgets/MobilePage/MobilePage"
export default {
  components: {
    Header,
    AdditionalSettingsBlock,
    ProductsListBlock,
    MobilePage,
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Bai+Jamjuree:wght@700&family=Inter&display=swap');

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

button {
  cursor: pointer;
}

.mobilePage {
  display: none;
}

.app {
  padding: 0 100px;
  min-width: 1440px;
}

.head {
  display: flex;
  justify-content: center;
}

.main {
  display: flex;
}

@media (min-width: 0px) and (max-width: 640px) {
  .desktopPage {
    display: none;
  }

  .mobilePage {
    display: block;
    width: 100%;
  }

  .app {
    padding: 0 16px;
    min-width: 375px;
  }
}
</style>
