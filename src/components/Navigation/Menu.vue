<template>
  <ul class="nav-links">
    <li v-for="item in menu" :key="item.id">
      <g-link :to="item.url">{{ item.text }}</g-link>
    </li>
  </ul>
</template>

<script>
export default {
  data () {
    return {
      menu: [
        {
          id: 1,
          text: "home",
          url: "/",
        },
        {
          id: 2,
          text: "about",
          url: "/about/",
        },
        {
          id: 3,
          text: "projects",
          url: "/projects/",
        },
        {
          id: 4,
          text: "blogs",
          url: "/blogs/",
        },
        {
          id: 5,
          text: "contact",
          url: "/contact/",
        },
      ]
    }
  },
}
</script>
