<template>
  <div :class="$style.AdvantagesText">
    <div :class="$style.title">Наше дело - труба. И это хорошо!</div>
    <div :class="$style.subtitle">
      По последним данным, только две категории людей<br/>
      улучшают ваше настроение с помощью труб: это сантехники<br/>
      и мы - музыканты
    </div>
  </div>
</template>

<script>
export default {
  name: 'AdvantagesText',
}
</script>

<style lang="scss" module>
  .AdvantagesText {
    margin-bottom: 6.4rem;
  }

  .title {
    text-align: center;
    font-family: 'Roboto Condensed', sans-serif;
    font-size: 4.8rem;
    line-height: 1;
    font-weight: 700;
    color: $primary;
  }

  .subtitle {
    margin-top: 3.2rem;
    text-align: center;
    font-size: 1.8rem;
    line-height: 1.2;
    color: $base-light-100;
  }
</style>
