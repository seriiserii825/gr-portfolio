<template>
  <Layout>
    <Hero/>
    <Services/>
    <Jobs/>
    <Projects :projects="$static.projects.edges" title="Featured projects" :showLink="true"/>
  </Layout>
</template>

<static-query>
{
  projects: allStrapiProject(filter: {featured: {eq: true}}) {
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
import Hero from "../components/Hero";
import Services from "../components/Services";
import Jobs from "../components/Jobs";
import Projects from "../components/Projects";

export default {
  components: {
    Jobs,
    Services,
    Hero,
    Projects
  },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
