<template>
  <AppHook v-if="showAppHook"></AppHook>
  <button @click="showAppHook = !showAppHook">
    Toggle
  </button>
  <h5>User</h5>
  {{ user.first_name }}
  {{ user.last_name }}
  <br><br>
  {{  fullName  }}

  <button @click="user.first_name = 'Sansa'">Atualizar</button>
</template>

<script>
import AppHook from './components/AppHook.vue'
import { ref, computed, watch } from 'vue'

export default {
  name: 'App',
  components: {
    AppHook
  },
  // No data() todos os componentes são reativos enquanto no setup não
  setup() {
    const user = ref({
      first_name: 'Jon',
      last_name: 'Snow'
    })

    const fullName = computed(() => {
      return `${user.value.first_name} ${user.value.last_name }`
    })

    watch(user, () => { // Essa é a maneira de reagir a uma ação watch em um objeto
      console.log('Logica cabulosa');
    }, {
      deep: true
    })

    watch(() => user.value.first_name, () => { // Essa é a maneira de reagir a uma ação watch em apenas um parametro do objeto
      console.log('Logica mas só em uma');
    }, {})


    const changeName = () => {
      alert('Chegou')
      user.value.first_name = 'Sansa'
    }

    const showAppHook = ref(true)

    return {
      name, changeName, user, fullName, showAppHook
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
