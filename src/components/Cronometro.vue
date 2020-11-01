<template>
  <div class="crono">
    <h3>Cuenta regresiva</h3>
    <div>
      <!-- Agregar un div que muestre la cuenta regresiva con v-show o if -->
      <div></div>
      <!-- Debo agragar un click a mis botones que llamen al método -->
      <button class="btn">3s</button>
      <button class="btn">1m</button>
      <button class="btn">5m</button>
      <button class="btn">10m</button>
      <button class="btn">30m</button>      
    </div>
  </div>
</template>

<script>
export default {
  name: 'Cronometro',
  data() {
    return {
      timers: [
      //Agregar los arrays
      ]
    }
  },
  // Agregar método para la cuenta regresiva. Almacenar y pasar la variable. Agregar booliano para que se activo el v-show
  // methods: {
  //   setUpTimer(){

  //   }    
  // },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn {
  margin: 4px;
}
</style>
