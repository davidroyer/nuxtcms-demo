<template>
  <b-navbar
    toggleable="sm"
    type="dark"
    variant="primary"
    class="navbar-expand-lg"
    sticky
  >
    <b-container>
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand to="/" exact>
        <h3><span class="fw-heavy">NuxtCMS</span> <small>Demo</small></h3>
      </b-navbar-brand>

      <b-collapse id="nav_collapse" is-nav>
        <b-navbar-nav v-for="leftMenu in leftMenus" :key="leftMenu.text">
          <b-nav-item :to="leftMenu.href">{{ leftMenu.text }}</b-nav-item>
        </b-navbar-nav>
      </b-collapse>

      <!-- 右侧菜单 -->
      <b-navbar-nav v-for="rightMenu in rightMenus" :key="rightMenu.text">
        <b-nav-item
          :href="rightMenu.href"
          :title="rightMenu.text"
          target="_blank"
          right
        >
          <img :src="rightMenu.img" class="rightImg" />
        </b-nav-item>
      </b-navbar-nav>
    </b-container>
  </b-navbar>
</template>

<script>
export default {
  data() {
    return {
      leftMenus: [
        {
          text: 'Project',
          href: '/projects'
        },
        {
          text: 'Blog',
          href: '/blog'
        }
      ],
      rightMenus: [
        {
          text: 'Github',
          img: './img/github.png',
          href: 'https://github.com/sharealex'
        },
        {
          text: '博客园',
          img: './img/cnblogs.png',
          href: 'http://www.cnblogs.com/sharealex'
        },
        {
          text: '新浪微博',
          img: './img/weibo.png',
          href: 'https://weibo.com/fugang521'
        },
        {
          text: 'QQ空间',
          img: './img/qqzone.png',
          href: 'https://user.qzone.qq.com/931571141'
        },
        {
          text: '网易邮箱',
          img: './img/wangyi.png',
          href: 'mailto:sharealex@163.com'
        }
      ]
    }
  }
}
</script>

<style scoped>
.navbar-nav-svg {
  display: inline-block;
  width: 20px;
  height: 20px;
  vertical-align: text-top;
}

.rightImg {
  width: 20px;
  height: 20px;
}

.fw-heavy {
  font-weight: 700;
}
</style>
