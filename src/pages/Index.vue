<template>
  <Layout>
    <Hero/>
    <Services/>
    <Jobs/>
    <Projects :projects="$static.projects.edges" title="Featured projects" :showLink="true"/>
    <AllBlogs :blogs="$static.blogs.edges" title="My blogs" :showLink="true"/>
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
  blogs: allStrapiBlog {
    edges {
      node {
        id
        title
        slug
        description
        image {
          url
        }
        category
        date(format: "MMMM Do, YYYY")
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
import AllBlogs from "../components/AllBlogs";

export default {
  components: {
    AllBlogs,
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
