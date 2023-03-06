<template>
  <div :class="$style.MainAdvantages">
    <div class="container">
      <AdvantagesText />
      <AdvantagesCardContainer :cards="cards"/>
    </div>
  </div>
</template>

<script>
import AdvantagesText from "@/components/advantages/AdvantagesText.vue";
import AdvantagesCardContainer from "@/components/advantages/AdvantagesCardContainer.vue";
export default {
  name: 'MainAdvantages',
  components: {
    AdvantagesText,
    AdvantagesCardContainer,
  },
  props: {
    cards: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style lang="scss" module>
  .MainAdvantages {
    padding-top: 8rem;
    padding-bottom: 8rem;
  }
</style>
