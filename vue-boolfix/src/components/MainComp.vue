<template>
    <main>
        <div class="cont-film">
            <h3 class="text-light ms-3">Film</h3>
            <FilmComp :filmsData="paramFilms" />
        </div> 
        <div class="cont-serie">
            <h3 class="text-light ms-3">Serie TV</h3>
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