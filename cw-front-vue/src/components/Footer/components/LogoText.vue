<template>
  <div class="LogoText">
    <img src="../assets/Logo-black.png" alt="">
  </div>
</template>

<script>

export default {
  name: "LogoText",
}
</script>

<style scoped>
.LogoText {
  margin-left: 310px;
  margin-top: 32px;
  height: 24px;
  width: 116px;
}

img {
  max-width: 100%;
}
@media screen and (max-width: 800px) {
  .LogoText{
    margin-left: 205px;
  }
}
@media screen and (max-width: 500px) {
  .LogoText{
    margin-left: 20px;
  }
}
</style>
