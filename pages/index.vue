<!-- 网站首页 -->
<template>
  <b-container fluid>
    <b-container>
      <br />
      <h2 class="card-text">
        The code for this demo is available on Github
      </h2>
      <b-button href="https://github.com/davidroyer/nuxtcms-demo">
        NuxtCMS Demo Repo</b-button
      >
      <!-- <b-card title="Github Repo">
        <p class="card-text">
          The code for this demo is available on Github
        </p>
        <b-link to="https://github.com/davidroyer/nuxtcms-demo">
          NuxtCMS Demo Repo</b-link
        >
      </b-card> -->
    </b-container>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      carouselImgs: [
        {
          img: 'https://picsum.photos/1110/416/?image=1',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=2',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=3',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=4',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=5',
          href: '/'
        },
        {
          img: 'https://picsum.photos/1110/416/?image=6',
          href: '/'
        }
      ]
    }
  }
}
</script>
