<template>
    <main>
        <div class="cont-film">
            <FilmComp :filmsData="paramFilms" />
        </div>
    </main>
</template>

<script>

import FilmComp from './FilmComp.vue';


export default{
    name: "MainComp",
    props: {
        paramFilms: Array
    },
    components: { 
        FilmComp 
    }
}

</script>

<style lang="scss">
main{
    background-color: #141414;
}
</style>