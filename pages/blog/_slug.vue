<template>
  <div>
    <b-button variant="primary" to="/blog"> Back To All Posts</b-button>
    <h1 v-text="post.title" />
    <img v-if="post.image" :src="imagePath" />
    <article v-html="post.html" />
  </div>
</template>

<script>
export default {
  computed: {
    imagePath() {
      return require(`~/assets/${this.post.image}`)
    }
  },
  asyncData({ $cmsApi, params }) {
    const post = $cmsApi.get('blog', params.slug)
    return { post }
  },

  head() {
    return {
      title: this.post.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.post.description || 'Default description here'
        }
      ]
    }
  }
}
</script>

<style>
img {
  max-width: 800px;
}
</style>
<style src="@droyer/nuxtcms/lib/assets/blog-styles.css"></style>
<style src="@@/node_modules/prismjs/themes/prism-tomorrow.css"></style>
