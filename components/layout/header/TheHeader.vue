<template>
  <div :class="[$style.TheHeader]">
    <div :class="[$style.headerContainer, 'container']">
      <HeaderLogo></HeaderLogo>
      <HeaderMenuDesktop :links="links"/>
      <HeaderContacts />
    </div>
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
    position: fixed;
    width: 100%;
    display: flex;
    align-items: center;
  }

  .headerContainer {
    position: relative;
    top: 0;
    z-index: 2;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 8rem;
    padding-top: 1.6rem;
    padding-bottom: 1.6rem;

    &:before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(14, 1, 20, .30);
      border-bottom-left-radius: .8rem;
      border-bottom-right-radius: .8rem;
      filter: blur(2px);
    }
  }
</style>
