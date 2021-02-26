<template>
  <div class="hero">
    <div class="section-center hero-center">
      <article class="hero-info">
        <div>
          <div class="underline"></div>
          <h1>I am John</h1>
          <h4>Freelance, web and UI designer</h4>
          <g-link to="/contact" class="btn">Contact me</g-link>
          <SocialLinks/>
        </div>
      </article>
      <g-image src="../assets/images/hero-img.png"/>
    </div>
  </div>
</template>

<script>
import SocialLinks from "./SocialLinks";

export default {
  components: {SocialLinks}
}
</script>

<style lang="scss">

</style>
