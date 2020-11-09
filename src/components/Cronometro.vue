<template>
  <div class="crono">
    <h3>Cuenta regresiva</h3>
    <div>
      <!-- mostrar conteo en el DOM -->
      <p>{{mostrarCuenta(tiempo)}}</p>
      <!-- Debo agregar un for in para llamar a cada objeto el array por cada botón y que llame al método que setea el intervalo -->
      <button class="btn" v-for="tpo in timers" :key="tpo" @click="contador(tpo.set)">{{tpo.nombre}}</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Cronometro',
  data() {
    return {
      tiempo: 0,
      intervalo: '',
      estado: {
        activo:false,
      },
      timers: [
        {nombre: '3s', set: 3},
        {nombre: '1m', set: 60},
        {nombre: '5m', set: 300},
        {nombre: '10m', set: 600},
        {nombre: '30m', set: 1800},
      ],

    }
  },
  // Agregar método para la cuenta regresiva. Almacenar y pasar las variables de minutos y segundos. Ocupar el setInterval de JS. Restar el tiempo.
  methods: {  
    mostrarCuenta: function (tiempo) {
      let segundos = ('0' + tiempo%60).slice(-2);
      let minutos = ('0' + Math.floor(tiempo/60)).slice(-2);
      return `${minutos}:${segundos}`
    },
    contador: function (setTime) {
      this.tiempo = setTime;
      this.estado.activo = true;
      this.intervalo = setInterval(() => {
        if (this.tiempo > 0) {
          this.tiempo --;
        }
        else {
          clearInterval(this.intervalo)
        }
      }, 1200);
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
