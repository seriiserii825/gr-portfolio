<template>
  <div class="section bg-grey">
    <Title title="Services"/>
    <div class="section-center services-center">
      <article v-for="item in services" :key="item.id" class="service">
        <component :is="item.icon"></component>
        <h4>{{ item.title }}</h4>
        <div class="underline"></div>
        <p>{{ item.text }}</p>
      </article>
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import ServicesIcon from './../assets/svg/services.svg';
import DesignIcon from './../assets/svg/design.svg';
import AppDesignIcon from './../assets/svg/app-design.svg';

export default {
  data () {
    return {
      services: [
        {
          id: 1,
          icon: DesignIcon,
          title: "web development",
          text: `I'm baby meditation tofu chillwave, distillery messenger bag thundercats chicharrones kale chips gochujang. Banh mi direct trade marfa salvia.`,
        },
        {
          id: 2,
          icon: ServicesIcon,
          title: "web design",
          text: `I'm baby meditation tofu chillwave, distillery messenger bag thundercats chicharrones kale chips gochujang. Banh mi direct trade marfa salvia.`,
        },
        {
          id: 3,
          icon: AppDesignIcon,
          title: "app design",
          text: `I'm baby meditation tofu chillwave, distillery messenger bag thundercats chicharrones kale chips gochujang. Banh mi direct trade marfa salvia.`,
        },
      ]
    }
  },
  components: {
    ServicesIcon,
    Title,
    DesignIcon,
    AppDesignIcon
  }
}
</script>

<style lang="scss">

</style>
