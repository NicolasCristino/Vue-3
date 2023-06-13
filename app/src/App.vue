<template>
  <h5>User</h5>
  {{ user.first_name }}
  {{ user.last_name }}
  <br><br>
  <h5>Admin</h5>
  {{ admin.first_name }}
  {{ admin.last_name }}
  <br><br>
  <img @click="changeName" alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import { ref, reactive } from 'vue'
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  // No data() todos os componentes são reativos enquanto no setup não
  setup() {
    const user = reactive({
      first_name: 'Jon',
      last_name: 'Snow'
    })

    const admin = ref({
      first_name: 'Admin',
      last_name: 'Master'
    })

    let name = 'Nicolas'

    const changeName = () => {
      alert('Chegou')
      name = 'Felipe'
      user.first_name = 'Sansa'
      admin.value.first_name = 'Stark'
    }

    return {
      name, changeName, user, admin
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
