<template>
    <div>
        <img :src="poster(info.backdrop_path)">
        <h2>{{info.title ? info.title : info.name}}</h2>
        <h3>{{info.original_title ? info.original_title : info.original_name}}</h3>
        <lang-flag :iso = "info.original_language" :alt= "info.original_language" class="d-block"/>
        <div>
            <h4>voto:</h4>
            <i class="fa-solid fa-star" v-for="(star, index) in stars(info.vote_average)" :key="index"></i>
            <i class="fa-regular fa-star" v-for="(starempty, index) in (5 - stars(info.vote_average))" :key="index" ></i>
        </div>

    </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: "BaseCard",
    props: {
       info: Object
    },
    components: {
        LangFlag,
    },

    methods: {
        poster(img) {
            return img == null ? "https://www.worldartfoundations.com/wp-content/uploads/2022/04/placeholder-image.png" : 'https://image.tmdb.org/t/p/w342/'+ img
        }, 

        stars(vote) {
            return Math.ceil((vote / 2));
        }
    }
}
</script>

<style lang="scss" scoped>
.flag-icon-undefined {
    background-image: url('../../assets/img/default.png');
}
</style>