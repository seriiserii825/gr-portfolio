<template>
  <ul class="social-links">
    <li v-for="item in socials" :key="item.id">
      <g-link :to="item.url">
        <component :is="item.icon"></component>
      </g-link>
    </li>
  </ul>
</template>

<script>
import Facebook from '~/assets/svg/facebook.svg';
import Twitter from '~/assets/svg/twitter.svg';
import Instagram from '~/assets/svg/instagram.svg';
console.log(Facebook);

export default {
  data () {
    return {
      socials: [
        {
          id: 1,
          icon: Facebook,
          url: "https://www.facebook.com",
        },
        {
          id: 2,
          icon: Twitter,
          url: "https://www.twitter.com",
        },
        {
          id: 3,
          icon: Instagram,
          url: "https://www.instagram.com",
        }
      ]
    }
  },
  components: {
    Facebook,
    Twitter,
    Instagram
  }
}
</script>

<style lang="scss">

</style>
