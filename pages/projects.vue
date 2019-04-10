<!-- 项目首页 -->
<template>
  <b-container fluid>
    <b-container class="projectTop" @click="toProjectHome">
      <h1>My Projects</h1>
      <p class="lead">
        This is my history project. You can click here to go back to the project
        list.
      </p>
    </b-container>

    <br />
    <nuxt-child />
  </b-container>
</template>

<script>
export default {
  scrollToTop: true,
  methods: {
    toProjectHome() {
      this.$router.push('/projects')
    }
  }
}
</script>

<style scoped>
.projectTop {
  cursor: pointer;
}
.projectTop:hover {
  color: rgb(141, 141, 141);
}
</style>
