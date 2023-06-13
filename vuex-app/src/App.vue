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
  {{ $store.state.user.first_name }} {{ $store.state.user.last_name }}
  <br><br> 
  <button @click="updateUser">
    Atualizar perfil
  </button>
  <br><br> 
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
      // this.$store.commit('storeUser', newUser)
      this.$store.dispatch('storeUser', newUser).then(() => {
        console.log('terminou');
      })
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
