<template>
  <Layout>
    <Hero/>
    <Services/>
  </Layout>
</template>

<script>
import Hero from "../components/Hero";
import Services from "../components/Services";

export default {
  components: {Services, Hero},
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
