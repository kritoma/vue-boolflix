<template>
  <section>
    <h1>FILM</h1>
    <div>
        <BaseCard v-for="(film, index) in dati.films" :key="index" :info="film"/>
    </div>
  </section>
</template>

<script>
import dati from '../../shared/dati';
import BaseCard from '../common/BaseCard.vue';

export default {
    name: "SectionFilm",
    components: { BaseCard },
    data() {
        return {
            dati,
        }
    }

}
</script>

<style lang="scss" scoped>
section {
  margin-bottom: 2.5rem;

  h1 {
    color: white;
  }

  div {
    display: flex;
    flex-wrap: wrap;
    gap: .625rem;
  }
}
</style>