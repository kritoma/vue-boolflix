<template>
   <div class="card">
        <ul>
            <li v-for="(film, index) in films" :key="index">
                <h2>{{film.title}}</h2>
                <h3>{{film.original_title}}</h3>
                <span>{{film.original_language}}</span>
                <span>{{film.vote_average}}</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "CardFilm",
    props: {
       films: Object
    }
}
</script>

<style lang="scss" scoped>

</style>