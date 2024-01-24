<template>
    <div>
      <!-- Swiper για Clubs -->
      <h2 style="text-align: center; color: #333; font-size: 1.5em; margin-bottom: 20px;">Για Club</h2>
      <div class="p-col-12 p-md-6 pt-2 swiper-container">
        <swiper :modules="modules"
         :spaceBetween="30" :centeredSlides="true" 
         :autoplay="{ delay: 3000, disableOnInteraction: false }" 
          class="mySwiper">
            <SwiperSlide>
                <img src="../../src/assets/images/club1.webp" alt="Image 1">
            </SwiperSlide>
            <SwiperSlide>
                <img src="../../src/assets/images/club2.webp" alt="Image 2">
            </SwiperSlide>
            <SwiperSlide>
                <img src="../../src/assets/images/club3.webp" alt="Image 3">
            </SwiperSlide>
        </swiper>
      </div>
  
      <!-- Swiper για Μπουζούκια -->
      <h2 style="text-align: center; color: #333; font-size: 1.5em; margin-bottom: 20px;">Για Μπουζούκια</h2>
      <div class="p-col-12 p-md-6 pt-2 swiper-container">
        <swiper :modules="modules" 
        :spaceBetween="30" 
        :centeredSlides="true"
        :autoplay="{ delay: 3500, disableOnInteraction: false }" 
         class="mySwiper">
            <SwiperSlide>
                <img src="../../src/assets/images/live1.webp" alt="Image 1">
            </SwiperSlide>
            <SwiperSlide>
                <img src="../../src/assets/images/live2.webp" alt="Image 2">
            </SwiperSlide>
            <SwiperSlide>
                <img src="../../src/assets/images/live3.webp" alt="Image 3">
            </SwiperSlide>
        </swiper>
      </div>
  
      <!-- Swiper για All Day Bar-Restaurants -->
      <h2 style="text-align: center; color: #333; font-size: 1.5em; margin-bottom: 20px;">Για All Day Bar-Restaurants</h2>

      <div class="p-col-12 p-md-6 pt-2 swiper-container">
        <swiper :modules="modules" 
        :spaceBetween="30" 
        :centeredSlides="true" 
        :autoplay="{ delay: 4000, disableOnInteraction: false }"  
        class="mySwiper">
            <SwiperSlide>
                <img src="../../src/assets/images/allday1.jpg" alt="Image 1">
            </SwiperSlide>
            <SwiperSlide>
                <img src="../../src/assets/images/allday2.jpg" alt="Image 2">
            </SwiperSlide>
            <SwiperSlide>
                <img src="../../src/assets/images/allday3.jpg" alt="Image 3">
            </SwiperSlide>
        </swiper>
      </div>
    </div>
</template>
  
<script>
import { Autoplay, Pagination, Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';


export default {
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      modules: [Autoplay, Pagination, Navigation]
    };
  }
};
</script>
  
<<style scoped>
.swiper-container {
    width: 100%;
    height: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.swiper-slide {
    display: flex;
    justify-content: center;
    align-items: center;
}

.swiper-slide img {
    width: 50%; 
    height: auto;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
</style>