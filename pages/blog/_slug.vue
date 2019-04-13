<template>
  <div>
    <b-button variant="primary" to="/blog"> Back To All Posts</b-button>
    <h1 class="page-title mb-5 mt-2 pt-3 text-center" v-text="post.title" />
    <img v-if="post.image" :src="imagePath" />
    <article class="markdown-body" v-html="post.html" />
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

<style lang="scss">
img {
  max-width: 800px;
}
article {
  width: 100%;

  &.markdown-body {
    a {
      color: var(--green);
    }
  }

  .custom-block p {
    margin-bottom: 16px;
    margin-top: 16px;
  }
}
</style>
<style src="@droyer/nuxtcms/lib/assets/blog-styles.css"></style>
<style src="@@/node_modules/prismjs/themes/prism-tomorrow.css"></style>
