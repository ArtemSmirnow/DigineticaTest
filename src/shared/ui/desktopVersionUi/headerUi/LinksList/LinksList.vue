<template>
  <div>
    <ul class="links">
      <li class="infoLink" v-for="link in links"><a href="">{{ link }}</a></li>
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

  .infoLink {
    font-size: 14px;
    font-family: 'Inter', sans-serif;
  }
}

a{
  outline: none;
  text-decoration: none;
  color: black;
}
a:hover{
  color: #125BAE;
}
</style>
