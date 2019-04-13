<template>
  <div>
    <b-navbar
      toggleable="sm"
      type="dark"
      variant="primary"
      class="navbar-expand-lg"
      sticky
    >
      <b-container>
        <b-navbar-brand to="/" exact>
          <h3 class="navbar-title">
            <span class="navbar-title-nuxtcms">NuxtCMS</span> Demo
          </h3>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item v-for="route in nav" :key="route.label" :to="route.to">
              {{ route.label }}
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>

<script>
export default {
  computed: {
    nav() {
      return this.$cmsApi.get('nav-menu')
    }
  }
}
</script>

<style lang="scss" scoped>
.nav-link {
  font-size: 1.2em;
  font-weight: 100;
}
.navbar-title {
  font-size: 1.75rem;
  margin-bottom: 0;
  &-nuxtcms {
    margin-right: 5px;
  }
}
</style>
