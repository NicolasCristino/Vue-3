<template>
  <TheHeader>
      <template v-slot:title>
        <h1>Home</h1>
      </template>
      <template v-slot:description>
        <p>Schwasneags</p>
      </template>
    Doggfather
  </TheHeader>

</template>

<script>
import TheHeader from './components/TheHeader.vue'

export default {
  mounted(){
    console.log(this.$slots)
  },
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
