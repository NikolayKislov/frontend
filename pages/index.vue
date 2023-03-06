<template>
  <div :class="$style.index">
    <TheHeader/>
    <HeroSlider :slides="slides"/>
    <MainAdvantages :cards="cards"/>
  </div>
</template>

<script>
import heroSlider from "assets/js/mocks/heroSlider";
import advantagesCards from "assets/js/mocks/advantagesCards";

import TheHeader from "~/components/layout/header/TheHeader.vue";
import HeroSlider from "@/components/hero/HeroSlider.vue";
import MainAdvantages from "@/components/advantages/MainAdvantages.vue";
export default {
  name: 'index',
  components: {
    TheHeader,
    HeroSlider,
    MainAdvantages
  },

  data() {
    return {
      slides: heroSlider.slider,
      cards: advantagesCards.cards,
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
