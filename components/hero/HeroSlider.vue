<template>
  <div :class="$style.HeroSlider">
    <div ref="slider" class="swiper" :class="$style.swiper">
      <div class="swiper-wrapper" :class="$style.swiperWrapper">
        <div class="swiper-slide" v-for="slide in slides" :class="$style.slide">
          <div :style="{'background-image': `url(${slide.slide})`}" :class="$style.slideImg"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper/js/swiper.min.js';
export default {
  name: 'HeroSlider',
  props: {
    slides: {
      type: Array,
      default: () => [],
    },
  },

  data() {
    return {
      sliderApp: null,
    };
  },

  mounted() {
    if (this.sliderApp) {
      this.sliderApp.destroy();
    }

    this.initSlider();
  },

  methods: {
    initSlider() {
      const options = {
        slidesPerView: 1,
        allowTouchMove:true,
        autoplay: true,
        speed: 5000,
        loop: true,
      };

      this.sliderApp = new Swiper(this.$refs.slider, options);
    },
  }
}
</script>

<style lang="scss" module>
  .HeroSlider {
    width: 100%;
    height: 100vh;
  }

  .swiper {
    height: 100%;
    overflow-y: hidden;
  }

  .swiperWrapper {
    height: 100%;
    display: flex;
  }

  .slide {
    width: 100vw;
    height: 100vh;
  }

  .slideImg {
    width: 100vw;
    height: 100vh;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
  }
</style>
