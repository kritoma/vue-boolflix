<template>
<main>
    <div>
        <ul>
            <li v-for="(film, index) in dati.films" :key="index">
                <h2>{{film.title}}</h2>
                <h3>{{film.original_title}}</h3>
                <span>{{film.original_language}}</span>
                <span>{{film.vote_average}}</span>
            </li>
        </ul>
    </div>
</main>
</template>

<script>

import dati from '../../shared/dati';

export default {
    name: "BaseMain",
    data() {
        return {
            dati,
        }
    },
   
}
</script>


<style lang="scss" scoped>

</style>