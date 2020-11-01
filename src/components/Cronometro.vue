<template>
  <div class="crono">
    <h3>Cuenta regresiva</h3>
    <div>
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
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn {
  margin: 4px;
}
</style>
