<template>
  <div id="app">
    <Header msg="I`m Header"/>
    <Footer msg="I`m Footer"/>
  </div>
</template>

<script>
import Header from "@/components/Header/Header";
import Footer from "@/components/Footer/Footer";

export default {
  name: 'App',
  components: {
    Footer,
    Header
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
@font-face {
  font-family: "Catamaran";
  src: local("Catamaran"),
  url(./fonts/catamaran.bold.ttf) format("truetype");
}
@font-face {
  font-family: "OpenSans";
  src: local("OpenSans"),
  url(./fonts/OpenSans-Regular.ttf) format("truetype");
}
</style>
