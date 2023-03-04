<template>
  <div :class="$style.HeaderLogo">
    <img src="/icons/header-logo.png" alt="" :class="$style.logo">
    <h1 :class="$style.title">MEGAPOLIS<br/>BRASS-BAND</h1>
  </div>
</template>

<script>
export default {
  name: 'HeaderLogo',


}
</script>

<style lang="scss" module>
  .HeaderLogo {
    display: flex;
    align-items: center;
    z-index: 2;
  }

  .logo {
    width: 6rem;
    height: 6rem;
    margin-right: 2.4rem;
  }

  .title {
    font-family: $font-title;
    font-size: 2.4rem;
    line-height: 1;
    font-weight: 600;
    color: $inversed;
  }
</style>
