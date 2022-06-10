<template>
<main>
   <SectionFilm/>
   <SectionTv/>
</main>
</template>

<script>
import SectionFilm from '../section/SectionFilm.vue';
import SectionTv from '../section/SectionTv.vue';

export default {
  components: { SectionFilm, SectionTv },
    name: "BaseMain",
    data() {
        return {
            
        }
    },
   
}
</script>


<style lang="scss" scoped>

</style>