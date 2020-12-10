<template>
  <div id="app">
    <TodoList v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'app',
  data(){
    return {
      todos: ['Зарядка', 'Завтрак', 'Разрядка', 'Перезарядка', 'Вне порядка', 'Ещё рифма на "рядка"']
    }
  },
  components: {
    TodoList
  },
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>


  ul{
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li{
    display: block;
    border: 2px solid #41b782;
    margin: 10px 0;
    padding: 10px 20px;
    cursor: pointer;
    width: 10rem;
    border-radius: 5px;
  }

  li:hover{
      background: #5cb88f33;
  }
</style>