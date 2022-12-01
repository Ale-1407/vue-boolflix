<template>
  <div id="app">
    <HeaderComp @emitSearch="searchFilms" />
    <MainComp :paramFilms="arrayFilms" :paramSerie="serieTv"/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'

import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
   
  },
  data(){
    return{
      arrayFilms: [],
      serieTv: []

    }
  },
  methods: {
    searchFilms(valoreEmit){

      axios.get( 'https://api.themoviedb.org/3/search/movie?api_key=cda4dbae7b4e0973efae2441cd54614c&query=' + valoreEmit )
      .then((response) => {
        this.arrayFilms = response.data.results
      })

      axios.get( 'https://api.themoviedb.org/3/search/tv?api_key=cda4dbae7b4e0973efae2441cd54614c&query=' + valoreEmit )
      .then((response) => {
        this.serieTv = response.data.results
      })
      
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #141414;
  height: 100vh;
}
</style>
