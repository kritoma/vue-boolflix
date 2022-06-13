<template>
  <section>
    <h2>SERIE TV</h2>
    <div>
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
section {
  
  h2{
    color: white;
  }

  div {
    display: flex;
    flex-wrap: wrap;
    gap: .625rem;
  }
}
</style>