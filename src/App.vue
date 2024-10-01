<template>
  <div>
    <h1>Page Home</h1>
    <p>------------------------------------------</p>
    <ParentComponent/>
    <ProductParent/>
    <CountParent/>
    <TodoApp/>
    <Modal/>
    <MessageParent/>
  </div>
  
</template>

<script setup>
  import ParentComponent from "./components/PrentComponent.vue"
  import ProductParent from "./components/ProductParent.vue";
  import CountParent from "./components/CountParent.vue";
import TodoApp from "./components/TodoApp.vue";
import Modal from "./components/Modal.vue";
import MessageParent from "./components/MessageParent.vue";
</script>

<style>

</style>