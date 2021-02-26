<template>
  <Layout>
    <Hero/>
    <Services/>
    <Jobs/>
  </Layout>
</template>

<script>
import Hero from "../components/Hero";
import Services from "../components/Services";
import Jobs from "../components/Jobs";

export default {
  components: {Jobs, Services, Hero},
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
