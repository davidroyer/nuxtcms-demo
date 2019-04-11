<template>
  <b-container fluid>
    <b-container class="blogTop" @click="$router.push('/blog')">
      <h1 class="page-title mb-5 mt-2 pt-3 text-center ">Blog Posts</h1>
      <p class="lead">
        This is my history post. You can click here to go back to the project
        list.
      </p>
    </b-container>

    <br />
    <b-container>
      <b-card-group columns>
        <nuxt-link
          v-for="post in blogPosts"
          :key="post.slug"
          :to="`/blog/${post.slug}`"
        >
          <b-card
            :title="post.title"
            :img-src="post.img"
            img-alt="Img"
            img-top
            class="project-card"
          >
            <p class="card-text" v-html="post.description"></p>
            <small class="text-muted" v-html="post.createTime"></small>
          </b-card>
        </nuxt-link>
      </b-card-group>
    </b-container>
    <nuxt-child />
  </b-container>
</template>

<script>
export default {
  asyncData({ $cmsApi }) {
    return { blogPosts: $cmsApi.get('blog') }
  }
}
</script>
