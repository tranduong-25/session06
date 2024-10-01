<!-- CountParent.vue -->
<template>
    <div>
      <h1>Count Parent Component</h1>
      <p>Current Count: {{ count }}</p>
      <CountChildren @increment="incrementCount" />
    </div>
  </template>
  
  <script>
  import CountChildren from './CountChildren.vue';
  
  export default {
    components: {
      CountChildren,
    },
    data() {
      return {
        count: 0, 
      };
    },
    methods: {
      incrementCount() {
        this.count++; 
      },
    },
  };
  </script>
  