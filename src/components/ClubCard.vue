<template>
    <Card class="p-3 flex flex-column">
      <img :src="club.logo" alt="Club Logo" class="mb-2" />
      <h3>{{ club.name }}</h3>
      <p>{{ club.address }}</p>
      <div class="flex justify-content-between">
        <div>
          <span>Απλό</span>
          <span>{{ club.simplePrice }}€</span>
        </div>
        <div>
          <span>Special</span>
          <span>{{ club.specialPrice }}€</span>
        </div>
      </div>
      <Rating :value="club.rating" readonly stars="6" />
      <Button label="Περισσότερα" icon="pi pi-info-circle" class="p-button-text" />
    </Card>
  </template>
  
  <script>
  import   Card  from 'primevue/card';
  import   Button  from 'primevue/button';
  import   Rating  from 'primevue/rating';
  
  export default {
    props: {
      club: {
        type: Object,
        required: true
      }
    },
    components: {
      Card,
      Button,
      Rating
    }
  }
  </script>
  
  <style scoped>
  /* Add styles if needed */
  </style>
  