<template>
  <div id="app">
    <Header/>
    <Content/>
    <Footer/>
  </div>
</template>

<script>
import Header from "@/components/Header/Header";
import Footer from "@/components/Footer/Footer";
import Content from "@/components/Content/Content";

export default {
  name: 'App',
  components: {
    Content,
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
  margin-top: 3px;
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
@font-face {
  font-family: "Catamaran-Black";
  src: local("OpenSans"),
  url(./fonts/Catamaran-Black.ttf) format("truetype");
}
</style>
