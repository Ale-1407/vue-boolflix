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
input{
  border-color: transparent;
}

input:hover{
  background-color: #be2e42;
  color: white;
  box-shadow: 0px 15px 20px rgba(255, 255, 255, 0.4);
}
</style>

