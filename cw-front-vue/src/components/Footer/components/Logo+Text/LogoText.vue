<template>
  <div class="LogoText">
    <Logo/>
    <TextField/>
  </div>
</template>

<script>
import Logo from "@/components/Footer/components/Logo+Text/Logo/Logo";
import TextField from "@/components/Footer/components/Logo+Text/Text/TextField";

export default {
  name: "LogoText",
  components: {
    TextField,
    Logo,
  }
}
</script>

<style scoped>
@media screen and (min-width: 300px) {
  .LogoText {
    margin: 40px 0 0 0;
    display: flex;
  }
}
@media screen and (min-width: 150px) and (max-width: 300px) {
  .LogoText {
    margin: 20px 0 42px 0;
    display: flex;
  }
}
@media screen and (max-width: 150px) {
  .LogoText {
    display: flex;
    margin-top: 24px;
  }
}
</style>
