<!-- 项目导航页面 -->
<template>
  <b-container>
    <b-card-group columns>
      <nuxt-link
        v-for="project in projects"
        :key="project.slug"
        :to="`projects/${project.slug}`"
      >
        <b-card
          :title="project.title"
          :img-src="project.img"
          img-alt="Img"
          img-top
          class="project-card"
        >
          <p class="card-text" v-html="project.description"></p>
          <small class="text-muted" v-html="project.createTime"></small>
        </b-card>
      </nuxt-link>
    </b-card-group>
  </b-container>
</template>

<script>
export default {
  asyncData({ $cmsApi }) {
    const projects = $cmsApi.get('projects')
    return { projects }
  }
}
</script>

<style scoped>
.project-card {
  cursor: pointer;
}

.project-card:hover {
  transform: scale(1.01);
}
</style>
