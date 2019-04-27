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
      <b-card-group deck>
        <b-card
          v-for="post in blogPosts"
          :key="post.slug"
          :title="post.title"
          :img-src="handlePostImage(post)"
          img-alt="Img"
          img-top
          class="post-card"
        >
          <!-- <nuxt-link :to="`/blog/${post.slug}`"> -->
          <p class="card-text" v-html="post.description"></p>
          <small class="text-muted" v-html="post.createTime"></small>
          <!-- </nuxt-link> -->

          <b-button :to="`/blog/${post.slug}`" variant="outline-primary"
            >View Post
          </b-button>
        </b-card>
      </b-card-group>
    </b-container>
    <!-- <nuxt-child /> -->
  </b-container>
</template>

<script>
export default {
  asyncData({ $cmsApi }) {
    return { blogPosts: $cmsApi.get('blog') }
  },
  methods: {
    handlePostImage(post) {
      return post.image
        ? require(`@/assets/images/${post.image}`)
        : require(`@/assets/images/post-2-hero.jpg`)
    }
  }
}
</script>

<style lang="scss" scoped>
.card-body {
  display: flex;
  flex-flow: column;
  justify-content: space-between;
  align-items: flex-start;
}
</style>
