<template>
    <div class="button-wrapper">
      <Button label="Κάνε Κράτηση" class="button-container p-button-success p-button-raised p-button-rounded" />
    </div>
  </template>
  
  <script>
  import Button from 'primevue/button';
  
  export default {
    components: {
      Button
    }
  }
  </script>
  
  <style scoped>
  .button-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .button-container {
    background-color: rgba(255, 204, 0) !important;
    color: rgb(24,27,29) !important;
    font-weight: bold;
    width: 200px; 
    height: 50px; 
    margin-top: 10px;
  }
  </style>