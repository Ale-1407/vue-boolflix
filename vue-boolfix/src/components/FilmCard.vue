<template>
    <div class="card bg-dark m-2">
        <img :src="`http://image.tmdb.org/t/p/w342/${singleFilm.poster_path}`"  alt="img">
        <div class="card-body d-flex flex-column">
           <span>Titolo: {{ singleFilm.title }}</span>
           <span>Titolo originale: {{ singleFilm.original_title }}</span>
           <span>Lingua: {{ singleFilm.original_language }}</span>
           <span>Voto: {{ singleFilm.vote_average }}</span>
           <span>Overview: {{ singleFilm.overview }}</span>
        </div>
    </div>
</template>

<script>

export default {
    name: 'FilmCard',
    props: {
        singleFilm: Object
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