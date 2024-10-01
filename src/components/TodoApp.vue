<!-- TodoApp.vue -->
<template>
    <div>
      <h1>Todo List</h1>
      <ul>
        <li v-for="todo in todos" :key="todo.id">
          <TodoItem :todo="todo" @delete-todo="handleDeleteTodo" />
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  import TodoItem from './TodoItem.vue';
  
  export default {
    components: {
      TodoItem
    },
    data() {
      return {
        todos: [
          { id: 1, text: 'Learn Vue.js' },
          { id: 2, text: 'Build a Todo App' },
          { id: 3, text: 'Deploy the App' }
        ]
      };
    },
    methods: {
      handleDeleteTodo(id) {
       
        this.todos = this.todos.filter(todo => todo.id !== id);
      }
    }
  };
  </script>
  
  <style scoped>
  
  </style>
  