<template>
  <div :class="{ 'nav-open': $store.state.navbar }">
    <MainNavbar />
    <nuxt />
    <MainFooter />
  </div>
</template>

<script>
import MainNavbar from '../components/MainNavbar.vue'
import MainFooter from '../components/MainFooter.vue'

export default {
  components: {
    MainNavbar,
    MainFooter,
  },
}
</script>
