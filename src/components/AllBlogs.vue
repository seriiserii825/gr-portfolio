<template>
  <section class="section">
    <Title :title="title"/>
    <section class="section-center blogs-center">
      <SingleBlog
        v-for="item in blogs"
        :key="item.node.id"
        :title="item.node.title"
        :slug="item.node.slug"
        :description="item.node.description"
        :image="item.node.image[0].url"
        :category="item.node.category"
        :date="item.node.date"
      />
    </section>
    <g-link to="/blogs" v-if="showLink" class="center-btn btn">Blogs</g-link>
  </section>
</template>

<script>
import SingleBlog from "./SingleBlog";
import Title from "./Title";

export default {
  props: {
    blogs: Array,
    title: String,
    showLink: Boolean
  },
  components: {Title, SingleBlog}
}
</script>

<style lang="scss">

</style>
