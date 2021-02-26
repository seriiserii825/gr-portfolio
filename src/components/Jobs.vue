<template>
  <section class="section job">
    <Title title="Experience"/>
    <div class="jobs-center">
      <div class="btn-container">
        <button
          @click="jobCount = item.node.number"
          class="job-btn"
          v-for="item in $static.jobs.edges"
          :key="item.node.id"
          :class="{'active-btn': item.node.number === jobCount}"
        >{{ item.node.company }}
        </button>
      </div>
      <div class="job-info">
        <div
          v-for="item in $static.jobs.edges"
          :key="item.node.id"
          v-if="item.node.number === jobCount"
        >
          <h3>{{ item.node.company }}</h3>
          <h4>{{ item.node.position }}</h4>
          <p class="job-date">{{ item.node.date }}</p>
          <div v-for="desc in item.node.description" :key="desc.name">{{ desc.name }}</div>
        </div>
      </div>
    </div>
  </section>
</template>
<static-query>
{
  jobs: allStrapiJob {
    edges {
      node {
        number
        id
        company
        position
        description {
          name
        }
      }
    }
  }
}
</static-query>
<script>
import Title from "./Title";

export default {
  data () {
    return {
      jobCount: 0,
    }
  },
  components: {Title}
}
</script>

<style lang="scss">

</style>
