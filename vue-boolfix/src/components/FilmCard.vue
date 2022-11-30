<template>
    <div class="card">
        <h5 class="card-title">{{ singleFilm.title }}</h5>
        <ul>
            <li>titolo originale: {{ singleFilm.original_title }}</li>
            <li>lingua: {{ singleFilm.original_language }}</li>
            <li>voto: {{ singleFilm.vote_average }}</li>
        </ul>
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