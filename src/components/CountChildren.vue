
<template>
    <div>
      <button @click="emitIncrement">Increment</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      emitIncrement() {
        this.$emit('increment'); 
      },
    },
  };
  </script>
  