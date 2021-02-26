<template>
  <nav class="navbar">
    <div class="nav-center">
      <div class="nav-header">
        <g-image src="../../assets/images/logo.svg" alt=""/>
      </div>
    </div>
    <Menu/>
  </nav>
</template>

<script>
import Menu from "./Menu";

export default {
  components: {Menu}
}
</script>
