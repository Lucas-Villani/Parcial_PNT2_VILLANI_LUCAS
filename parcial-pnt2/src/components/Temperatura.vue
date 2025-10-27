<template>
  <div>
    <label>Ingrese Temperatura °C</label>
    <input
      type="number"
      v-model.number="celsius"
      placeholder="Ingrese temperatura"
    />

    <p :style="{ color: colorTexto }">
      Conv Temperatura °F: {{ fahrenheit }}
    </p>

    <p :style="{ color: colorTexto }">
      Conv Temperatura °K: {{ kelvin }}
    </p>
  </div>

  <div>
    <p>Respuestas: 1: C / 2: C / 3: A </p>
  </div>
</template>

<script>
export default {
  name: "Temperatura",
  data() {
    return {
      celsius: 0,
    };
  },
  computed: {
    fahrenheit() {
      return (this.celsius * 9) / 5 + 32;
    },
    kelvin() {
      return this.celsius + 273.15;
    },
    colorTexto() {
      if (this.celsius <= 0) return "blue";
      else if (this.celsius < 15) return "magenta";
      else return "red";
    },
  },
};
</script>

<style scoped>
input {
  margin-left: 10px;
  width: 80px;
  font-size: 16px;
  padding: 3px;
}
</style>
