<template>
  <div>
    <b-button variant="primary" to="/blog"> Back To All Posts</b-button>
    <h1 class="page-title mb-5 mt-2 pt-3 text-center" v-text="post.title" />
    <img v-if="post.image" class="post-image" :src="postImage" />
    <article class="article-content" v-html="post.html" />
  </div>
</template>

<script>
export default {
  computed: {
    postImage() {
      return require(`@/assets/images/${this.post.image}`)
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

  &.post-image {
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    display: block;
    width: 100%;
    max-width: 100%;
    margin-bottom: 3rem;
    margin-top: -1.75rem;
  }
}
article {
  width: 100%;

  &.article-content {
    a {
      color: var(--green);
    }
  }
  h1 {
    margin-top: 3rem;
  }

  h2 {
    margin-top: 2.75rem;
  }

  h3 {
    margin-top: 1.5rem;
  }
  .custom-block p {
    margin-bottom: 16px;
    margin-top: 16px;
  }
}
</style>
<style src="@droyer/nuxtcms/lib/assets/blog-styles.css"></style>
<style src="@@/node_modules/prismjs/themes/prism-tomorrow.css"></style>
