<template>
  <div id="app">
  <NavbarComponent />
    <div id="carousel-container" class="relative">
      <div class="w-full h-[60vh] md:h-[80vh] relative overflow-hidden">
        <div
          class="carousel-inner flex transition-all duration-500"
          :style="{ transform: 'translateX(-' + currentIndex * 100 + '%)' }"
        >
          <div
            v-for="(image, index) in images"
            :key="index"
            class="w-full h-full flex-shrink-0"
          >
            <img
              class="w-full h-full object-cover"
              :src="image.src"
              alt="Carousel image"
            />
            <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-center text-white">
              <h4 class="text-xl font-semibold mb-2">{{ image.subtitle }}</h4>
              <h1 class="text-4xl md:text-5xl font-bold mb-4">{{ image.title }}</h1>
              <a href="#" class="btn bg-blue-500 text-white py-3 px-6 rounded-lg">
                Learn More
              </a>
            </div>
          </div>
        </div>

        <button
          @click="prevImage"
          class="absolute top-1/2 left-0 transform -translate-y-1/2 bg-black bg-opacity-50 text-white p-2 rounded-full"
        >
          &#10094;
        </button>
        <button
          @click="nextImage"
          class="absolute top-1/2 right-0 transform -translate-y-1/2 bg-black bg-opacity-50 text-white p-2 rounded-full"
        >
          &#10095;
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import NavbarComponent from './components/NavbarComponent.vue';

export default {
  name: 'App',
  components: {
    NavbarComponent,
  },
  data() {
    return {
      currentIndex: 0,
      images: [
        {
          src: "@/assets/carousel-1.jpg",
          subtitle: "Laundry & Dry Cleaning",
          title: "Best For Laundry Services",
        },
        {
          src: "@/assets/carousel-2.jpg",
          subtitle: "Laundry & Dry Cleaning",
          title: "Highly Professional Staff",
        },
        {
          src: "@/assets/carousel-3.jpg",
          subtitle: "Laundry & Dry Cleaning",
          title: "Fast and Reliable Service",
        },
      ],
    };
  },
  mounted() {
    this.carouselInterval = setInterval(this.nextImage, 5000);
  },
  beforeUnmount() {
    clearInterval(this.carouselInterval);
  },
  methods: {
    nextImage() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
    prevImage() {
      this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
    },
  },
};
</script>

<style scoped>
.carousel-inner {
  display: flex;
}
</style>
