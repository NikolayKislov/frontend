<template>
  <div :class="$style.index">
    <TheHeader/>
    <HeroSlider :slides="slides"/>
  </div>
</template>

<script>
import TheHeader from "~/components/layout/header/TheHeader.vue";
import heroSlider from "assets/js/mocks/heroSlider";
import HeroSlider from "@/components/hero/HeroSlider.vue";
export default {
  name: 'index',
  components: {
    TheHeader,
    HeroSlider
  },

  data() {
    return {
      slides: heroSlider.slider,
    }
  }
}
</script>

<style lang="scss" module>
.index {
  width: 100%;
  height: 100vh;
  background-color: $inversed;
}
</style>
