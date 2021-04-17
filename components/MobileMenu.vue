<template>
  <md-list
    class="nav-mobile-menu nav-mobile-section-start"
    v-if="navMobileSectionStart"
  >
    <slot></slot>
  </md-list>
</template>

<script>
export default {
  name: "MobileMenu",
  props: {
    navMobileSectionStart: {
      type: Boolean,
      default: false
    }
  }
};
</script>
