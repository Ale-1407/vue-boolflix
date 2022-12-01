<template>
    <main>
        <div class="cont-film">
            <h2 class="text-light ms-3 mb-4 fw-bold">Film</h2>
            <FilmComp :filmsData="paramFilms" />
        </div> 
        <div class="cont-serie">
            <h2 class="text-light ms-3 mt-4 fw-bold">Serie TV</h2>
            <SerieTvComp :serieData="paramSerie" />
        </div>   
            
        
    </main>
</template>

<script>

import FilmComp from './FilmComp.vue';
import SerieTvComp from './SerieTvComp.vue';

export default{
    name: "MainComp",
    props: {
        paramFilms: Array,
        paramSerie: Array
    },
    components: { 
        FilmComp,
        SerieTvComp
    }
}

</script>

<style lang="scss">
main{
    background-color: #141414;
}
</style>