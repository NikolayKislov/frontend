<template>
  <div :class="$style.AdvantagesCardContainer">
    <AdvantagesCard
      v-for="card in cards"
      :key="card.label"
      :card="card"
    />
  </div>
</template>

<script>
import AdvantagesCard from "@/components/advantages/AdvantagesCard.vue";
export default {
  name: 'AdvantagesCardContainer',
  components: {
    AdvantagesCard,
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
  .AdvantagesCardContainer {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
  }
</style>
