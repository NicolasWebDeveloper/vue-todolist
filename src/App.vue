<template>
  <h1>Todo - List</h1>
  <input type="text" v-model="currentInput" />
  <button @click="addTodo">Add</button>
  <ul>
    <todo-item v-for="todo in todos" v-bind:key="todo" :todo-text="todo"></todo-item>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      currentInput: '',
      todos: [],
    };
  },
  methods: {
    addTodo() {
      this.todos.push(this.currentInput);
      this.currentInput = '';
    },
  },
};
</script>
