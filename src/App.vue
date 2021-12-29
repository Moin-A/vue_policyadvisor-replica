<template>
  <Header/>
  <TopSection/>
  <Features/>
 
</template>

<script>

import Header from "./components/Header.vue"
import TopSection from "./components/SectionWidget.vue"
import Features from "./components/section-features.vue"
export default {
  name: "App",
  components: {
    Header,
    TopSection,
    Features

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
