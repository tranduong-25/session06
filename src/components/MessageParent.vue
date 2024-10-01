<!-- MessageParent.vue -->
<template>
    <div>
      <h2>Parent Component</h2>
  
      <!-- Sử dụng component con và lắng nghe sự kiện 'message-sent' -->
      <MessageChildren @message-sent="handleMessage" />
  
      <!-- Hiển thị thông báo khi nhận được sự kiện -->
      <p v-if="message">{{ message }}</p>
    </div>
  </template>
  
  <script>
  import MessageChildren from './MessageChildren.vue';
  
  export default {
    name: 'MessageParent',
    components: {
      MessageChildren
    },
    data() {
      return {
        message: ''  // Biến để lưu thông báo từ component con
      };
    },
    methods: {
      handleMessage(msg) {
        // Nhận thông báo từ sự kiện và hiển thị trên màn hình
        this.message = msg;
      }
    }
  };
  </script>
  
  <style scoped>
  h2 {
    font-size: 1.5rem;
    margin-bottom: 16px;
  }
  p {
    font-size: 1.25rem;
    color: green;
  }
  </style>
  