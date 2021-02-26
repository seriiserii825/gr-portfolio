<template>
  <g-link :to="`/blogs/${slug}`" class="blog">
    <article>
      <div class="blog-img">
        <img :src="adminUrl+image" alt="">
      </div>
      <div class="blog-card">
        <h4>{{ title }}</h4>
        <p>{{ description }}</p>
        <div class="blog-footer">
          <p>{{ category }}</p>
          <p>{{ date }}</p>
        </div>
      </div>
    </article>
  </g-link>
</template>

<script>
export default {
  props: {
    title: String,
    slug: String,
    description: String,
    image: String,
    category: String,
    date: String
  },
  data () {
    return {
      adminUrl: process.env.GRIDSOME_ADMIN_URL
    }
  }
}
</script>

<style lang="scss">

</style>
