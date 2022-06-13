<template>
  <div>
    <form @submit.prevent="searchtv()">
        <input type="text" placeholder="Search" v-model="search">
        <button type="submit">Search</button>
    </form>
  </div>
</template>

<script>
import dati from '../../shared/dati';
import axios from 'axios';

export default {
    name: "SearchFilm",
    data() {
        return {
          search:"",
          dati,
        }
    },
    methods: {
      searchtv() {
        dati.films = [];
        axios.get('https://api.themoviedb.org/3/search/movie', {
          params: {
            api_key: '76ea54f3a12656613e82010a935b694d',
            query: this.search,
            language: 'it-IT'
          }
        }).then((response) => {
            console.log(response.data.results)
            dati.films = response.data.results
        }).catch((error) => {
            console.log(error)
        });

        dati.serieTv = [];
        axios.get('https://api.themoviedb.org/3/search/tv', {
          params: {
             api_key: '76ea54f3a12656613e82010a935b694d',
            query: this.search,
            language: 'it-IT'
          }
        }).then((response) => {
            console.log(response.data.results)
            dati.serieTv = response.data.results
        }).catch((error) => {
            console.log(error)
        });

        this.search = "";
      },
    },
        
    
}
</script>

<style lang="scss" scoped>

</style>