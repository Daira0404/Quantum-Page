<template>
  <div id="app">
    <NavbarComponent />
    <Carousel :items-to-show="1" :autoplay-speed="3000" :wrap-around="true">
      <slide v-for="slide in slides" :key="slide.image">
        <img :src="slide.image" style="width: 100%; margin-top: -18px">
        <h1 style="position: absolute; left: 90px">{{ slide.text }}</h1>
      </slide>
      <template #addons>
        <Navigation />
        <Pagination />
      </template>
    </Carousel>
    <div class="container-service ">
          <div class="box-service">afaf</div>
          <div class="box-service">aefae</div>
          <div class="box-service">aefefa</div>
          <div class="box-service">afeaef</div>
          <div class="box-service">aefaef</div>
    </div>
  </div>
</template>

<script>
import NavbarComponent from './components/NavbarComponent.vue';
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

export default {
  name: 'App',
  components: {
    NavbarComponent,
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      slides: [
        {
          image: require('@/assets/carousel-1.jpg'),  
          text: 'Laundry Service'
        },
        {
          image: require('@/assets/carousel-2.jpg'),  
          text: 'Dry Cleaning Service'
        },
        {
          image: require('@/assets/carousel-3.jpg'),  
          text: 'Ironing Service'
        }
      ]
    }
  }
};
</script>
<style>
  .container-service {
    position: absolute;
    left: 10%;
    width: 80%;
    margin: -105px auto 0 auto;
    display: flex;
    flex-wrap: wrap;
    gap: 1.5px;
    z-index: 1;
  }

  .box-service {
    flex: 1 1 18%;
    height: 150px;
    background-color: #f0f0f0;
    transition: background-color 0.3s ease;
    border-radius:5px;
  }

  .box-service:hover {
    background-color: #184286;
    height: 200px;
    transform: translateY(-25px);
  }
</style>