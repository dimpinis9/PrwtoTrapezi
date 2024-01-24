<template>
  <nav class="nav-container flex align-items-center justify-content-between p-3 text-white"
  style="background-color: rgb(24,27,29);">
      <div class="title-container">
      <h1 style="color: rgba(255, 204, 0);">PrwtoTrapezi.gr</h1>
        </div>
        <div class="menu-button">
          <i class="pi pi-bars" style="color:rgba(255, 204, 0) ;" v-if="isSmallScreen && !isMenuOpen" @click="openMenu"></i>
          <div class="flex align-items-center">
          <i class="pi pi-times" style="color:rgba(255, 204, 0) ;" v-if="isSmallScreen && isMenuOpen" @click="closeMenu"></i>
          <div class="menu-container flex gap-3" v-else-if="isMenuOpen || !isSmallScreen" style="font-weight:bold ;">
          <router-link to="/" style="color:rgba(255, 204, 0) ;">Home</router-link>
          <router-link to="/clubs" style="color:rgba(255, 204, 0) ;">Clubs</router-link>
          <router-link to="/bars" style="color:rgba(255, 204, 0) ;">Mpouzoukia</router-link>
          <router-link to="/allday" style="color:rgba(255, 204, 0) ;">All-Day Bar-Restaurants</router-link>
          <router-link to="/contact" style="color:rgba(255, 204, 0) ;">Contact</router-link>
          </div>
          </div>
        </div>
      </nav>
</template>
  
  <script>
  import  Button  from 'primevue/button';
  
  export default {
    components: {
      Button
    },
    data() {
    return {
      isSmallScreen: false,
      isMenuOpen: false
    };
  },
  methods: {
    openMenu() {
      this.isMenuOpen = true;
    },
    closeMenu() {
      this.isMenuOpen = false;
    }
  },
  mounted() {
    this.isSmallScreen = window.innerWidth <= 600;
    window.addEventListener('resize', () => {
      this.isSmallScreen = window.innerWidth <= 600;
      if (!this.isSmallScreen) {
        this.isMenuOpen = false;
      }
    });
  }
}
</script>
  
<style scoped>
@media (max-width: 600px) {
  .nav-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .title-container {
    order: 1;
  }
  .menu-container {
    order: 2;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
  }
  .menu-button {
    order: 3;
  }
  
}
</style>