<template>
  <section class="section projects">
    <Title :title="title"/>
    <div class="section-center projects-center">
      <Project
        v-for="(project, index) in projects"
        :key="project.node.id"
        :index="index"
        :title="project.node.title"
        :description="project.node.description"
        :image="project.node.image.url"
        :github="project.node.github"
        :url="project.node.url"
        :skills="project.node.skills"
      />
    </div>
    <g-link to="/projects" class="btn center-btn" v-if="showLink">Projects</g-link>
  </section>
</template>

<script>
import Title from './Title';
import Project from './Project';

export default {
  props: {
    projects: Array,
    title: String,
    showLink: Boolean
  },
  components: {
    Title,
    Project
  }
}
</script>

<style lang="scss">
</style>
