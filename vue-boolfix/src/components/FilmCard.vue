<template>
    <div class="card bg-dark m-2">
        <div class="image">
            <img :src="`http://image.tmdb.org/t/p/w342/${singleFilm.poster_path}`"  alt="img">
        </div>
        
        <div class="card-body">
            <div class="card-text d-flex flex-column">
                <div>
                    <span class="fw-semibold">Titolo: </span>
                    <span class="font"> {{ singleFilm.title }}</span>
                </div>
                <div>
                    <span class="fw-semibold">Lingua: </span>
                    <span class="font"> {{ singleFilm.original_language }}</span>
                    <img :src=" `https://www.countryflagicons.com/SHINY/64/.png`" alt="img">
                </div>
                <div>
                    <span class="fw-semibold">Voto: </span>
                    <span class="font"> {{ singleFilm.vote_average }}</span>
                </div>
                <div>
                    <span class="fw-semibold">Overview: </span>
                    <span class="font"> {{ singleFilm.overview }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'FilmCard',
    props: {
        singleFilm: Object
    },
    
}
</script>

<style lang="scss">

.card{
    width: calc( 100% / 6);
    cursor: pointer;
}

.card:hover{
    box-shadow: 0px 15px 20px rgba(190, 46, 66, 0.5);
}

.card-body{
    background-color: black;
    display: none;
}

.font{
    font-size: 14px;
}

.card-body span{
    color: white;
}

.image{
    display: block;
    width: 100%;
}

.image img{
    width: 100%;
    display: block;
    height: 380px;
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