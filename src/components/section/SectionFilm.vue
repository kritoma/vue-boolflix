<template>
  <section>
    <h1>Film</h1>
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

</style>