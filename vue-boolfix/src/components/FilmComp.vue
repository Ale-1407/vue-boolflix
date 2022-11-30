<template>
    <div>
        <FilmCard v-for="(elem, index) in filmsData" :key="index" :singleFilm="elem" />
    </div>
</template>

<script>

import FilmCard from './FilmCard.vue'

export default {
    name: 'FilmComp',
    props: {
        filmsData: Array
    },
    components: {
        FilmCard
    }

}
</script>