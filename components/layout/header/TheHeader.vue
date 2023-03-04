<template>
  <div :class="[$style.TheHeader, 'container']">
    <HeaderLogo></HeaderLogo>
    <HeaderMenuDesktop :links="links"/>
    <HeaderContacts />
  </div>
</template>

<script>
//mocks
import headerLinks from '~/assets/js/mocks/headerLinks.js';

//components
import HeaderLogo from "~/components/layout/header/HeaderLogo.vue";
import HeaderMenuDesktop from "@/components/layout/header/HeaderMenuDesktop.vue";
import HeaderContacts from "@/components/layout/header/HeaderContacts.vue";

export default {
  name: 'TheHeader',
  components: {
    HeaderLogo,
    HeaderMenuDesktop,
    HeaderContacts,
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
    justify-content: space-between;
    height: 8rem;
    padding-top: 2rem;
  }
</style>
