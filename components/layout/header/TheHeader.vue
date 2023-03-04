<template>
  <div :class="[$style.TheHeader, 'container']">
    <HeaderLogo></HeaderLogo>
    <HeaderMenuDesktop :links="links"/>
  </div>
</template>

<script>
//mocks
import headerLinks from '~/assets/js/mocks/headerLinks.js';

//components
import HeaderLogo from "~/components/layout/header/HeaderLogo.vue";
import HeaderMenuDesktop from "@/components/layout/header/HeaderMenuDesktop.vue";

export default {
  name: 'TheHeader',
  components: {
    HeaderLogo,
    HeaderMenuDesktop,
  },

  data() {
    return {
      links: headerLinks.links,
    };
  },
}
</script>

<style lang="scss" module>
  .TheHeader {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    height: 8rem;
    padding-top: 2rem;
  }
</style>
