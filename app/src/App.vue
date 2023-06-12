<template>
  <div>
    <UXAlert :variant="variant" :text="text" @close="onClose()" v-if="showAlert"></UXAlert> <!--Componente manipulado por CSS de escopo-->
  </div>
</template>

<script>
import UXAlert from './components/UXAlert.vue'

export default {
  name: 'App',
  components: {
    UXAlert
  },
  data() {
    return{
      variant: 'danger',
      text: 'Formulário enviado',
      showAlert: true
    }
  },


  methods:{
    onClose() {
      this.showAlert = !this.showAlert
      console.log('teste pai')
    }
  },

  computed: {
  },

  watch: {

  },

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
.acess{
  color: green;
  font-weight: bolder;
}
</style>
