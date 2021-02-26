<template>
  <Layout>
    <Projects :projects="$static.projects.edges" title="My projects" :showLink="false"/>
  </Layout>
</template>

<static-query>
{
  projects: allStrapiProject {
    edges {
      node {
        id
        title
        description
        image {
          url
        }
        github
        url
        featured
        skills {
          title
        }
      }
    }
  }
}
</static-query>
<script>
import Projects from "../components/Projects";

export default {
  components: {
    Projects
  }
}
</script>

<style lang="scss">
</style>
