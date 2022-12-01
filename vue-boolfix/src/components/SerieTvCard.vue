<template>
    <div class="card bg-dark m-2">
        <img :src="`http://image.tmdb.org/t/p/w342/${singleSerie.poster_path}`" alt="img">
        <div class="card-body d-flex flex-column">
           <span>Titolo: {{ singleSerie.name }}</span>
           <span>Titolo originale: {{ singleSerie.original_name}}</span>
           <span>Lingua: {{ singleSerie.original_language }}</span>
           <span>Voto: {{ singleSerie.vote_average }}</span>
           <span>Overview: {{ singleSerie.overview }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SerieTvCard',
    props: {
        singleSerie: Object
    }
}
</script>

<style lang="scss">

.card{
    width: calc( 100% / 6);
    cursor: pointer;  
}

.card-body{
    background-color: black;
}

.card-body span{
    color: white;
}

</style>