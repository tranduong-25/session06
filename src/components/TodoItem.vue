<!-- TodoItem.vue -->
<template>
    <div>
      <span>{{ todo.text }}</span>
      <button @click="deleteTodo">Delete</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      todo: {
        type: Object,
        required: true
      }
    },
    methods: {
      deleteTodo() {
       
        this.$emit('delete-todo', this.todo.id);
      }
    }
  };
  </script>
  
  <style scoped>
 
  </style>
  