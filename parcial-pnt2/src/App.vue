<template>
  <div id="app">
    <h1>Conversor de Temperaturas</h1>
    <hr />
    <Temperatura />
  </div>
</template>

<script>
import Temperatura from './components/Temperatura.vue';

export default {
  name: 'App',
  components: {
    Temperatura,
  },
};
</script>

<style>

</style>
