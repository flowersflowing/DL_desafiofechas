<template>
  <div class="crono">
    <h3>Cuenta regresiva</h3>
    <div>
      <!-- Agregar un div que muestre la cuenta regresiva con v-show o if. Debe mostrar {{timer.tiempo}}.-->
      <div></div>
      <!-- Debo agregar un click a mis botones que llamen al método -->
      <button class="btn" @click="setUpTimer(3000)">3s</button>
      <button class="btn" @click="setUpTimer(60000)">1m</button>
      <button class="btn" @click="setUpTimer(300000)">5m</button>
      <button class="btn" @click="setUpTimer(600000)">10m</button>
      <button class="btn" @click="setUpTimer(1800000)">30m</button>      
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
        {nombre: '3', tiempo: '00:03'},
        {nombre: '1', tiempo: '01:00'},
        {nombre: '5', tiempo: '05:00'},
        {nombre: '10', tiempo: '10:00'},
        {nombre: '30', tiempo: '30:00'},
      ]
    }
  },
  // Agregar método para la cuenta regresiva. Almacenar y pasar la variable. Agregar booliano para que se active el v-show
  methods: {
    setUpTimer(ms){
      console.log(ms); //entrando
    }    
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn {
  margin: 4px;
}
</style>
