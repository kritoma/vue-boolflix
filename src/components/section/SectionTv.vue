<template>
  <section>
      <div>
        <h2>Serie Tv</h2>
        <BaseCard v-for="(tv, index) in dati.serieTv" :key="index" :info="tv"/>
    </div>
  </section>
</template>

<script>
import BaseCard from '../common/BaseCard.vue';
import dati from '../../shared/dati';

export default {
    name: "SectionTv",
    components: { BaseCard },
    data() {
        return {
            dati,
        }
    }
}
</script>

<style lang="scss">

</style>