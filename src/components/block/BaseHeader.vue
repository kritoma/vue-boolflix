<template>
  <header>
    <img src="../../assets/img/Netflix-Logo.jpg" alt="Netflix-logo">
    <SearchFilm/>
  </header>
</template>

<script>
import SearchFilm from '../common/SearchFilm.vue';

export default {
  components: { SearchFilm },
    name: "BaseHeader",
}
</script>

<style lang="scss" scoped>
header {
  background-color: #000000;
  display: flex;
  align-items: center;
  justify-content: space-between;

  img {
    height: 100px;
  }
}
</style>