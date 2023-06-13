<template>
  <AppProduct></AppProduct>
  {{ name }}
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AppProduct from './components/Products/AppProduct.vue'

export default {
  name: 'App',
  components: {
    HelloWorld, AppProduct
  },
  // No data() todos os componentes são reativos enquanto no setup não
  setup() {
    const name = 'Nicolas'

    return {
      name
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
