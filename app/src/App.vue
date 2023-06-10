<template>
        <div>
            <input type="text" v-model="name">
            <br>
            {{ name }}
        </div>
        <div>
            <input type="text" v-model="user.first_name">
            <br>
            <input type="text" v-model="user.last_name">
            <br>
            {{ user.first_name }} {{ user.last_name }}
        </div>

</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return{
      name: '',
      user: {
        first_name: '',
        last_name: '',
      },
    }
  },
  methods:{
    saveUserName(){
      console.log('Ajax'); 
      console.log(this.name);
    }
  },

  computed: {
  },

  watch: {
    name(value) {
      if(value.length >= 3){
        this.saveUserName()
      }
    },
    user: {
      handler(){
        console.log('User alterado');
      },
      deep: true
    }
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
