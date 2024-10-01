<!-- Modal.vue -->
<template>
    <div v-if="isVisible" class="modal-backdrop">
      <div class="modal">
        <div class="modal-header">
          <h3>{{ title }}</h3>
          <button @click="closeModal">X</button>
        </div>
        <div class="modal-content">
          <!-- Slot để hiển thị nội dung truyền từ component cha -->
          <slot></slot>
        </div>
        <div class="modal-footer">
          <button @click="closeModal">Close</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      },
      isVisible: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      closeModal() {
        // Phát sự kiện để thông báo đóng modal
        this.$emit('close');
      }
    }
  };
  </script>
  
  <style scoped>
  .modal-backdrop {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal {
    background: white;
    padding: 20px;
    border-radius: 8px;
    max-width: 500px;
    width: 100%;
  }
  
  .modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .modal-content {
    margin: 20px 0;
  }
  
  .modal-footer {
    text-align: right;
  }
  </style>
  