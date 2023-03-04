<template>
  <div :class="$style.HeaderMenuDesktop">
    <ul :class="$style.linksContainer">
      <li v-for="link in links" :key="link.label">
        <a :href="link.link" :class="$style.link">{{ link.label }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HeaderMenuDesktop',
  props: {
    links: {
      type: Array,
      default: () => [],
    }
  }
}
</script>

<style lang="scss" module>
  .HeaderMenuDesktop {
    width: 100%;
    max-width: 60rem;
  }

  .linksContainer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }

  .link {
    position: relative;
    font-size: 2.4rem;
    line-height: 1;
    font-weight: 400;
    color: $inversed;

    &:before {
      content: "";
      position: absolute;
      left: 0;
      top: calc(100% + 1px);
      width: 0;
      height: 3px;
      background-color: $inversed;
      transition: width ease-in-out .3s;
    }

    &:hover:before {
      width: 100%;
    }
  }
</style>
