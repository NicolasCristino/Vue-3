<template>
        <div>
            Two-way data binding
            v-model -> formulários
        </div>
        <br>

        <div class="">
            <label for="">Nome</label> <br>
            <input type="text" v-model="name">
            <br><br>
            {{ name }}
        </div>
        
        <br><br>

        <div>
          <label for="">Sports</label> <br>
          <select v-model="sports">
            <option value="">Selecione</option>
            <option value="futebol">Futebol</option>
            <option value="basquete">Basquete</option>
            <option value="volei">Volei</option>
          </select> <br> <br>
          {{ sports }}
        </div>

        <br><br>

        <div>
          <label for="">Newsletter</label> <br>
          <input type="radio" value="Sim" v-model="newsletter"> Sim
          <input type="radio" value="Não" v-model="newsletter"> Não
          <br> <br>
          {{ newsletter }}
        </div>

        <br><br>

        <div>
          <label for="">Newsletter</label> <br>
          <input type="checkbox" value="Amarelo" v-model="checkbox"> Amarelo
          <input type="checkbox" value="Azul" v-model="checkbox"> Azul
          <input type="checkbox" value="Vermelho" v-model="checkbox"> Vermelho
          <br> <br>
          {{ checkbox }}
        </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return{
      name:'',
      sports: '',
      newsletter: '',
      checkbox: []
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
