<template>
  <div :class="[$style.TheHeader, 'container']">
    <HeaderLogo></HeaderLogo>
  </div>
</template>

<script>
import HeaderLogo from "~/components/layout/header/HeaderLogo.vue";
export default {
  name: 'TheHeader',
  components: {
    HeaderLogo,
  }

}
</script>

<style lang="scss" module>
  .TheHeader {
    height: 8rem;
    padding-top: 2rem;
  }
</style>
