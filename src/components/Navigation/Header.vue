<template>
  <nav class="navbar">
    <div class="nav-center">
      <div class="nav-header">
        <g-link to="/">
          <g-image src="../../assets/images/logo.svg" alt=""/>
        </g-link>
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
