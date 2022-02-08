<template>
  <div class="Header">
    <LogoImage/>
    <Menu/>
  </div>
</template>

<script>


import LogoImage from "@/components/Header/components/LogoImage";
import Menu from "@/components/Header/components/Menu";

export default {
  name: "Header",
  components: {Menu, LogoImage},
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
  }
}
</style>
