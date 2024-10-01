<!-- MessageChildren.vue -->
<template>
    <div>
      <button @click="sendMessage">Send message</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MessageChildren',
    methods: {
      sendMessage() {
        this.$emit('message-sent', 'Message from child component');
      }
    }
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #2980b9;
  }
  </style>
  