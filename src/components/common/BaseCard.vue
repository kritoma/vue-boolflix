<template>
    <div class="card">
        <img :src="poster(info.backdrop_path)">
        <div class="opacity">
            <div class="content">
                <h2>Titolo:{{info.title ? info.title : info.name}}</h2>
                <h3>Titolo originale:{{info.original_title ? info.original_title : info.original_name}}</h3>
                <lang-flag :iso = "info.original_language" :alt= "info.original_language" class="d-block"/>
                <div>
                    <h4>voto:</h4>
                    <i class="fa-solid fa-star" v-for="(star, index) in stars(info.vote_average)" :key="index"></i>
                    <i class="fa-regular fa-star" v-for="(starempty, index) in (5 - stars(info.vote_average))" :key="index" ></i>
                </div>
                <p>{{info.overview}}</p>
            </div>
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

.card {
    position: relative;
    width: 342px;
    border-radius: 10px;
    opacity: 1;
    cursor: pointer;
    border: 1px solid black;




    .opacity {
        background-color: black;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        transition: all .25s ease;
        opacity: 0;
        overflow: auto;
    }
   
    &:hover .opacity{
        opacity: 0.9;
    }

    &:hover .content {
        opacity: 1;
    }
    
    img {
        width: 100%;
    }

    .content {
        position: absolute;
        top: 0;
        left: 0;
        padding: 10px;
        opacity: 0;
        transition: all .25s ease;
        color: white;
        font-size: 18px;
        overflow: auto;
        z-index: 10;
        
        i{
            color: yellow;
        }
    }
}
</style>