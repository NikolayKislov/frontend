<template>
  <div :class="$style.index">
    <TheHeader/>
  </div>
</template>

<script>
import TheHeader from "~/components/layout/header/TheHeader.vue";
export default {
  name: 'index',
  components: {
    TheHeader,
  },
}
</script>

<style lang="scss" module>
.index {
  width: 100%;
  height: 100vh;
  background-color: $primary;
}
</style>
