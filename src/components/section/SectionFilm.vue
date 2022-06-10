<template>
  <section>
      <CardFilm :films="dati.films"/>
  </section>
</template>

<script>
import CardFilm from '../common/CardFilm.vue';
import dati from '../../shared/dati';

export default {
    name: "SectionFilm",
    components: { CardFilm },
    data() {
        return {
            dati,
        }
    }

}
</script>

<style lang="scss" scoped>

</style>