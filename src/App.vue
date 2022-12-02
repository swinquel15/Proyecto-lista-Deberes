<template>
  <div>
    <div id="header"></div>
    <div id="main-container">
      <h2>Todos</h2>
      <TodosWeb v-bind:todoslist="copyTodosWeb"/>
    </div>
  </div>
</template>

<script>

//import SearchWeb from './components/SearchWeb'
import TodosWeb from './components/TodosWeb';
//import TodoAdd from './components/TodoAdd'
export default {
  name: 'App',
  components: {
    TodosWeb
  },
  data(){
    return{
      todos:[
        {
          id: 0,
          title:'comprar la cena',
          completed:false
        },
        {
          id: 1,
          title:'Sacar a pasear al perro',
          completed:true
        },
        {
          id:2,
          title:'jugar Xbox',
          completed:false
        }
      ],
      copyTodosWeb:[]
    }
  },
  created(){
    this.copyTodosWeb=[...this.todos];
  }
}
</script>

<style>
  *{
    box-sizing: border-box;
  }
  body{
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1.5em;
    padding: 0;
    margin: 0;
  }
  #main-container{
    border: solid 1px #ccc;
    width: 600px;
    margin: 100px auto;
  }
  #header{
    background: black;
    padding: 10px;
  }
  h2{
    padding: 0 10px;
  }
</style>
