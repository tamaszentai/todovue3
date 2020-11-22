<template>
  <h1>Todo</h1>
  <input v-model="todoInput">
  <button @click="addTodo">Add todo</button>
  <ul>
    <li v-for="(todo,index) in todos" :key="index">
      {{todo}}
      </li>

  </ul>
</template>

<script>
export default {
  data() {
    return {
      todos: [],
    todoInput: '',
  }
},
methods: {
addTodo() {
  this.todos.push(this.todoInput);
  this.todoInput= '';
  console.log(this.todos);
}
}
  
}
</script>

<style lang="stylus" scoped></style>