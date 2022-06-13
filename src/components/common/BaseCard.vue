<template>
    <div>
        <img src="" alt="">
        <h2>{{info.title ? info.title : info.name}}</h2>
        <h3>{{info.original_title ? info.original_title : info.original_name}}</h3>
        <lang-flag :iso = "info.original_language" :alt= "info.original_language" class="d-block"/>
        <span>{{info.vote_average}}</span>
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
    }
}
</script>

<style lang="scss" scoped>
.flag-icon-undefined {
    background-image: url('../../assets/img/default.png');
}
</style>