<template>
  <div>
    <AppHeader />
    <br />
    <nuxt />
    <br />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
import AppFooter from '@/components/AppFooter.vue'

export default {
  components: {
    AppHeader,
    AppFooter
  },
  scrollToTop: true
}
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
}
* {
  outline: none;
  user-select: none;
}
.page-enter-active,
.page-leave-active {
  transition: opacity 0.3s ease-in-out;
}
.page-enter,
.page-leave-active {
  opacity: 0;
}
</style>
