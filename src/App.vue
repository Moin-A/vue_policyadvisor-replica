<template>
  <LayoutDefault>
  <TopSection/>
  <Features/>
  <Section_Review/>
  </LayoutDefault>
 
</template>

<script>


import TopSection from "./components/Sections/SectionWidget.vue"
import Features from "./components/Sections/section-features.vue"
import LayoutDefault from "./components/Layouts/Default_layout.vue"
import Section_Review from "./components/Sections/Section-review.vue"

export default {
  name: "App",
  components: {
    LayoutDefault,
    TopSection,
    Features,
    Section_Review


  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
@font-face {
  font-family: "lato";
  src: url("./fonts/Lato/Lato-Bold.ttf");
}
</style>
