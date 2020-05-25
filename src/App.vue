<template>
  <div id="app">
    <header class="d-flex justify-content-center flex-column align-items-center pb-5">
      <h1 class="py-5">Desafío 4</h1>
      <h2>Introducción a VueJS</h2>
    </header>

    <Cuenta-regresiva></Cuenta-regresiva>
    
  </div>
</template>

<script>
import CuentaRegresiva from './components/Cuenta-regresiva.vue';

export default {
  name: "App",
  data() {
    return {

      }
  },
  components: {
    CuentaRegresiva
  }
};
</script>