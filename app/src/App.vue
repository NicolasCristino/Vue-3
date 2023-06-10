<template>
  <TheHeader v-show="showHeader"/>
        <div>
          <h2>Ola</h2>
          {{ name }}
        </div> <br>

        <button @click="showHeader = !showHeader">
          Mostrar ou esconder Header
        </button>

</template>

<script>
import TheHeader from './components/TheHeader.vue'

export default {
  name: 'App',
  components: {
    TheHeader
  },
  data() {
    return{
      name: 'Robb',
      showHeader: true,
    }
  },

  // $el é a raíz do componente, o elemento child do template
  beforeCreate(){
    console.log('beforeCreate')
    console.log('Estado:',this.name)
    console.log('DOM:',this.$el)
  },

  created(){
    console.log('created')
    console.log('Estado:',this.name)
    console.log('DOM:',this.$el)
  },

  beforeMount(){
    console.log('beforeMount')
    console.log('Estado:',this.name)
    console.log('DOM:',this.$el)
  },

  mounted(){
    console.log('mounted')
    console.log('Estado:',this.name)
    console.log('DOM:',this.$el)
  },

  beforeUnmount(){
    console.log('beforeUnmount')
    console.log('Estado:',this.name)
    console.log('DOM:',this.$el)
  },

  unmounted(){
    console.log('unmounted')
    console.log('Estado:',this.name)
    console.log('DOM:',this.$el)
  },


  methods:{

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
