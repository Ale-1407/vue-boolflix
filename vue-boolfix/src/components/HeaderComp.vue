<template>
    <header class="d-flex justify-content-between align-items-center p-3">
        <div>
          <h2 class="text-danger fw-semibold">BOOLFLIX</h2>
        </div>
        <div class="d-flex">
            <input type="text" v-model="searchInput" placeholder="Cerca"
            @keyup="$emit( 'emitSearch', searchInput )">
        </div>
        
    </header>
</template>

<script>

export default {
  name: 'HeaderComp',
  data() {
    return{
        searchInput: ''
    }
  }
}
</script>

<style lang="scss">

header{
  background-image: linear-gradient(black, #141414) ;
}
</style>

