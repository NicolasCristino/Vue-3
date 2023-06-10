<template>
  <div>
    <HelloWorld></HelloWorld> <!--Componente manipulado por CSS de escopo-->
    <BaseCard></BaseCard> <!--Componente manipulado por CSS global em ./assets/css/style.css-->
  </div>
</template>

<script>
import BaseCard from './components/BaseCard.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  mounted(){
    console.log(this.$slots)
  },
  name: 'App',
  components: {
    BaseCard, HelloWorld
  },
  data() {
    return{
      name: 'Robb',
      showHeader: true,
    }
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
