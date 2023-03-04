<template>
  <div :class="$style.HeaderContacts">
    <div
      :class="$style.activeLabel"
      @mouseenter="show = true"
    >
      Связаться с нами
    </div>
    <transition name="fade">
      <div
        v-if="show" :class="$style.dropdown"
        @mouseleave="show = false"
      >
        <a
          :class="$style.link"
          href="tel:+7999999999"
          @click="show = false"
        >
          Позвонить
        </a>
        <a :class="$style.link"
           href="mailto: test@mail.ru"
           @click="show = false"
        >
          Написать
        </a>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'HeaderContacts',
  data() {
    return {
      show: false,
    };
  },
}
</script>

<style lang="scss" module>
  .HeaderContacts {
    position: relative;
  }

  .activeLabel {
    font-size: 2.4rem;
    line-height: 1;
    font-weight: 400;
    color: $inversed;
    cursor: pointer;
  }

  .dropdown {
    position: absolute;
    top: 3rem;
    display: flex;
    flex-direction: column;
    width: 100%;
    padding: 2.4rem;
    box-shadow: 0 10px 10px rgba(14, 14, 41, .05);
    border-radius: .8rem;
    background-color: $inversed;
  }

  .link {
    font-size: 2.4rem;
    line-height: 1;
    font-weight: 400;
    color: $secondary;
  }
</style>
