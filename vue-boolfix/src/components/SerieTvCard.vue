<template>
    <div class="card bg-dark m-2">
        <div class="image">
            <img :src="`http://image.tmdb.org/t/p/w342/${singleSerie.poster_path}`" alt="img">
        </div>
        <div class="card-body">
            <div class="card-text d-flex flex-column">
                <div>
                    <span class="fw-semibold">Titolo: </span>
                    <span class="font"> {{ singleSerie.name }}</span>
                </div>
                <div>
                    <span class="fw-semibold">Lingua: </span>
                    <span class="font"> {{ singleSerie.original_language }}</span>
                </div>
                <div>
                    <span class="fw-semibold">Voto: </span>
                    <span class="font"> {{ singleSerie.vote_average }}</span>
                </div>
                <div>
                    <span class="fw-semibold">Overview: </span>
                    <span class="font"> {{ singleSerie.overview }}</span>
                </div>
            </div>          
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
    background-color: rgba(0, 0, 0, 0.7);
    display: none;
}

.card-body span{
    color: white;
}

.image img{
    width: 100%;
    display: block;
    height: 380px;
}

.card:hover img{
    display: none;
}

.card:hover .card-body{
    display: block;
    overflow-y: scroll;
    height: 300px;
}

::-webkit-scrollbar {
    width: 3px;
  }
  
  /* Track */
  ::-webkit-scrollbar-track {
    background: #141414; 
    border-radius: 5px;
  }
   
  /* Handle */
  ::-webkit-scrollbar-thumb {
    background: rgb(182, 182, 182); 
    border-radius: 5px;
  }
  
  /* Handle on hover */
  ::-webkit-scrollbar-thumb:hover {
    background: rgb(125, 125, 125); 
  }

</style>