<template>
        <div>
          <button @click="onclick">
            Enviar
          </button>
        </div>

        <div @mouseover="onMouseOver">
          Passa o mouse aqui
        </div>
        <br><br>

        <form action="" @submit.once="onSubmit">
          <button type="submit">Enviar</button>
        </form>
        <br><br>

        <input type="text" @keyup="onKeyup">
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return{

          }
  },
  methods:{
    onclick() {
      alert('click')
    },
    onMouseOver($evt){
      console.log('Hoverizou', $evt)
    },
    onSubmit(){
      console.log('Submitou')
    },
    onKeyup($evt){
      console.log('Teclou meu mano', $evt)
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
.acess{
  color: green;
  font-weight: bolder;
}
</style>
