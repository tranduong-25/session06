
  
  

  
<template>
    <div>
      <h1>Product Parent Component</h1>
      <ProductChildren :product="product" />
    </div>
  </template>
  
  <script setup>
  import ProductChildren from './ProductChildren.vue';
  
  const product = {
    id: 1,
    name: 'Bưởi Ba Roi',
    price: '12.000 đ',
    quantity: 10,
  };
  </script>
  
  