<template>
  <LayoutDefault>
  <TopSection/>
  <Features/>
  </LayoutDefault>
 
</template>

<script>


import TopSection from "./components/SectionWidget.vue"
import Features from "./components/section-features.vue"
import LayoutDefault from "./components/Layouts/Default_layout.vue"

export default {
  name: "App",
  components: {
    LayoutDefault,
    TopSection,
    Features,


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
