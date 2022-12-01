<template>
    <div class="card bg-dark m-2">
        <div class="image">
            <img :src="`http://image.tmdb.org/t/p/w342/${singleFilm.poster_path}`"  alt="img">
        </div>
        
        <div class="card-body">
            <div class="card-text d-flex flex-column">
                <span>Titolo: {{ singleFilm.title }}</span>
                <span>Titolo originale: {{ singleFilm.original_title }}</span>
                <span>Lingua: {{ singleFilm.original_language }}</span>
                <span>Voto: {{ singleFilm.vote_average }}</span>
                <span>Overview: {{ singleFilm.overview }}</span>
            </div>
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
    display: none;
}

.card-body span{
    color: white;
}

.image{
    display: block;
    width: 100%;
}

.image:hover{
    display: none;
}

.card-body:hover{
    display: block;
    overflow-y: scroll;
    height: 300px;
}

::-webkit-scrollbar {
    width: 3px;
  }
  
  /* Track */
  ::-webkit-scrollbar-track {
    background: #f1f1f1; 
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