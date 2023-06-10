<template>
        <div>
          {{ fullName }} <br> <br>
        </div>

        <h2>Todos em aberto</h2>

        <div v-for="todo in uncompletedTodos" :key="todo.id">
           {{ todo.title }} <span>{{ todo.completed }}</span>
        </div>

        <h2>Todos completas</h2>

        <div v-for="todo in completedTodos" :key="todo.id">
           {{ todo.title }} <span>{{ todo.completed }}</span>
        </div>

</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return{
      user: {
        first_name: 'Robb',
        last_name: 'Stark',
      },
      todos: [
          {
            "userId": 1,
            "id": 1,
            "title": "delectus aut autem",
            "completed": false
          },
          {
            "userId": 1,
            "id": 2,
            "title": "quis ut nam facilis et officia qui",
            "completed": false
          },
          {
            "userId": 1,
            "id": 3,
            "title": "fugiat veniam minus",
            "completed": false
          },
          {
            "userId": 1,
            "id": 4,
            "title": "et porro tempora",
            "completed": true
          },
          {
            "userId": 1,
            "id": 5,
            "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
            "completed": false
          },
          {
            "userId": 1,
            "id": 6,
            "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
            "completed": true
          }
        ]
    }
  },
  methods:{
  },

  computed: {
    fullName(){
      return `${this.user.first_name} ${this.user.last_name}`
    },

    uncompletedTodos(){
      return this.todos.filter(todo => !todo.completed);
    },

    completedTodos(){
      return this.todos.filter(todo => todo.completed);
    },
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
