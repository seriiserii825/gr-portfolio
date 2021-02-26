<template>
  <Layout>
    <AllBlogs :blogs="$static.blogs.edges" title="My blogs" :showLink="false"/>
  </Layout>
</template>
<static-query>
{
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
import AllBlogs from "../components/AllBlogs";

export default {
  components: {AllBlogs}
}
</script>

<style lang="scss">

</style>
