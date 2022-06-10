<template>
    <div class="card">
        <ul>
            <li v-for="(tv, index) in serieTv" :key="index">
                <h2>{{tv.name}}</h2>
                <h3>{{tv.original_name}}</h3>
                <span>{{tv.original_language}}</span>
                <span>{{tv.vote_average}}</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "CardTv",
    props: {
        serieTv: Object,
    }
}
</script>

<style>

</style>