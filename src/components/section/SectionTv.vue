<template>
  <div>
      <CardTv :serieTv="dati.serieTv"/>
  </div>
</template>

<script>
import CardTv from '../common/CardTv.vue';
import dati from '../../shared/dati';

export default {
    name: "SectionTv",
    components: { CardTv },
    data() {
        return {
            dati,
        }
    }
}
</script>

<style lang="scss">

</style>