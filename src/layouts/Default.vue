<template>
  <div class="layout">
    <Header/>
    <slot/>
  </div>
</template>
<script>
import Header from "../components/Navigation/Header";

export default {
  components: {Header}
}
</script>
