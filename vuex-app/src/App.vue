<template>
  {{ $store.getters.total }}
  <AppProducts />
  <br><br>
  <br><br>

  <pre>
    {{ $store.state.cart }}
  </pre>

  
  <br><br>
  <br><br>
  <button @click="updateUser">
    Atualizar perfil
  </button>
</template>

<script>
import AppProducts from '@/components/products/AppProducts.vue'

export default {
  name: 'App',
  components: {
    AppProducts
  },
    data(){
      return {
      }
    },
    created(){
      
    },
  methods: {
    updateUser() {
      const newUser = {
        first_name: 'Robb',
        last_name: 'Stark',
        email: 'robb@stark.com',
      } 
      this.$store.commit('storeUser', newUser)
      console.log(this.$store)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: start;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
