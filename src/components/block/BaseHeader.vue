<template>
  <header>
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
  background-color: #2c2c2c;
  padding: 1.25rem;
}
</style>