<template>
    <div class="flex align-items-center justify-content-center p-5" 
    style="background: linear-gradient(to right, rgb(24,27,29), rgb(31, 36, 39);">
      <InputText placeholder="Ψάχνω Τραπέζι...." />
      <Button @click="search" class="ml-2" 
      style="background-color: rgba(255, 204, 0); color: rgb(24,27,29); font-weight: bold; border: 2px black">
      Αναζήτηση</Button>
    </div>
  </template>
  
  <script>
  import  InputText  from 'primevue/inputtext';
  import  Button  from 'primevue/button';
  
  export default {
    components: {
      InputText,
      Button
    }
  }
  </script>
  
  <style scoped>
  /* Add styles if needed */
  </style>
  