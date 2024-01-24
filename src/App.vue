<template>
  <div>
    <NavBar />
    <SearchArea />
    <OrderButton />
        <Swiper />
      </div>
    
  
</template>

<script>
import NavBar from './components/NavBar.vue';
import SearchArea from './components/SearchArea.vue';
import Swiper from './components/Swiper.vue';
import OrderButton from './components/OrderButton.vue';

export default {
  components: {
    NavBar,
    SearchArea,
    Swiper,
    OrderButton
  },
  data() {
    return {
      clubs: [
        {
          id: 1,
          name: 'Blast Athens Club',
          address: 'Evmolpidon 11, Athina 118 54',
          logo: 'path_to_logo_image',
          simplePrice: 120,
          specialPrice: 170,
          rating: 6
        },
        // Add more club objects here
      ]
    }
  }
}
</script>
