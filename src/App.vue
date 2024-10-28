<template>
  <div id="app">
    <h1>Számok szorzása</h1>
    <div>
      <label for="number1">Első szám:</label>
      <input type="number" v-model="number1" id="number1" />
    </div>
    <div>
      <label for="number2">Második szám:</label>
      <input type="number" v-model="number2" id="number2" />
    </div>
    <button @click="multiplyNumbers">Számok összeszorzása</button>
    <div v-if="result !== null">
      <h2>Eredmény: {{ result }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number1: 0,
      number2: 0,
      result: null,
    };
  },
  methods: {
    multiplyNumbers() {
      this.result = this.number1 * this.number2;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

input {
  margin-bottom: 10px;
}
</style>


