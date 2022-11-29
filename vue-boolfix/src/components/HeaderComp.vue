<template>
    <header class="bg-dark d-flex justify-content-between align-items-center p-3">
        <div>
          <h2 class="text-danger fw-semibold">BOOLFLIX</h2>
        </div>
        <div class="d-flex">
            <input type="text">
            <button class="ms-3">Cerca</button>
        </div>
        
    </header>
</template>

<script>

export default {
  name: 'HeaderComp',
  components: {

  }
}
</script>

<style lang="scss">

button{
    border: transparent;
}

button:hover{
    background-color: rgba(255, 0, 0, 0.7);
}

</style>