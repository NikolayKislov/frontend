<template>
  <div :class="$style.AdvantagesCard">
    <div :class="$style.cardImage" :style="{'background-image': `url(${card.image})`}"></div>
    <div :class="$style.cardLabel">
      <span :class="$style.labelText">{{ card.label }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AdvantagesCard',
  props: {
    card: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>

<style lang="scss" module>
  .AdvantagesCard {
    position: relative;
    overflow: hidden;
    width: 45rem;
    height: 40rem;
    border-radius: .8rem;
    cursor: pointer;

    &:hover {
      .cardLabel {
        top: 70%;
      }
    }
  }

  .cardImage {
    width: 100%;
    height: 100%;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
    transition: all ease-in-out .3s;

    &:hover {
      transform: scale(1.05);
    }
  }

  .cardLabel {
    position: absolute;
    z-index: 1;
    top: 100%;
    left: 0;
    width: 100%;
    height: 30%;
    padding: 2.4rem;
    background-color: rgba(0, 0, 0, .75);
    transition: all ease-in-out .5s;
  }

  .labelText {
    font-size: 2.4rem;
    line-height: 1;
    color: $inversed;
  }
</style>
