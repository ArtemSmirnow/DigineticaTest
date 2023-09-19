<template>
  <div>
    <ul class="links">
      <li class="li" v-for="link in links">{{ link }}</li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      links: ['Информация о компании', 'Контакты', 'Полезные ссылки'],
    }
  }
}
</script>
<style scoped>
.links {
  margin-left: 24px;
  display: flex;
  width: 400px;
  list-style-type: none;
  align-items: center;
  font-family: 'Inter', sans-serif;
  height: 17px;
  gap: 20px;

  .li {
    font-size: 14px;
    font-family: 'Inter', sans-serif;
  }
}
</style>
