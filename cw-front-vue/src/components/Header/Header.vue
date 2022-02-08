<template>
  <div class="Header">
    <LogoImage/>
    <Menu/>
<!--    <ChangeLanguage/>-->
  </div>
</template>

<script>


import LogoImage from "@/components/Header/components/LogoImage";
import Menu from "@/components/Header/components/Menu";
// import ChangeLanguage from "@/components/Header/components/ChangeLanguage";

export default {
  name: "Header",
  components: {Menu, LogoImage, /*ChangeLanguage*/},
}
</script>

<style scoped>
.Header {
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: flex-start;
  background: white;
  color: #1e1e1e;
  height: 144px;
  padding: 1em;
}
@media screen {
  .Header {
    display: flex;
    align-content: center;
    align-items: center;
    justify-content: space-between;
    background: white;
    color: #1e1e1e;
    height: 144px;
    padding: 1em;
  }
}
</style>
