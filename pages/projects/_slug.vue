<!-- 项目子页 -->
<template>
  <b-container>
    <h1 class="page-title mb-5 mt-2 pt-3 text-center" v-text="project.title" />
    <div v-html="project.html" />
  </b-container>
</template>

<script>
export default {
  asyncData({ $cmsApi, params }) {
    const project = $cmsApi.get('projects', params.slug)
    return { project }
  }
}
</script>
