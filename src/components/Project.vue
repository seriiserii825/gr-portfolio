<template>
  <article class="project">
    <div class="project-img">
      <img :src="adminUrl+image" alt="">
    </div>
    <div class="project-info">
      <span class="project-number">0{{ index + 1 }}</span>
      <h3>{{ title }}</h3>
      <p class="project-desc">{{ description }}</p>
      <div class="project-stack">
        <span v-for="item in skills" :key="item.title">{{ item.title }}</span>
      </div>
      <div class="project-links">
        <a v-if="github" target="_blank" :href="github">
          <GitHubSvg/>
        </a> <a target="_blank" :href="url">
        <SiteSvg/>
      </a>
      </div>
    </div>
  </article>
</template>

<script>
import GitHubSvg from './../assets/svg/github.svg';
import SiteSvg from './../assets/svg/site.svg';

export default {
  props: {
    index: Number,
    title: String,
    description: String,
    image: String,
    github: String,
    url: String,
    skills: Array
  },
  data () {
    return {
      adminUrl: process.env.GRIDSOME_ADMIN_URL
    }
  },
  components: {
    GitHubSvg,
    SiteSvg
  }
}
</script>

<style lang="scss">
</style>
