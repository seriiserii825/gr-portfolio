<template>
  <div class="section-title">
    <h2>{{ title || 'Default title' }}</h2>
    <div class="underline"></div>
  </div>
</template>

<script>
export default {
  props: {
    title: String
  }
}
</script>

<style lang="scss">

</style>
