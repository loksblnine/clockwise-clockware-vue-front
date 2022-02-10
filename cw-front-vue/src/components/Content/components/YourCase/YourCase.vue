<template>
  <div class="TextButton">
    <h3>Discuss your project
      with<br> the professionals
      <span></span></h3>
    <Button msg="Let’s discuss"/>
  </div>
</template>

<script>
import Button from "@/components/Content/components/Button/Button";

export default {
  name: "YourCase",
  components: {
    Button
  }
}
</script>

<style scoped>
.TextButton {
  margin-left: 20px;
}

.TextButton > h3 {
  text-transform: uppercase;
  font-family: Catamaran-Black;
  font-size: 25px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.2;
  letter-spacing: -0.63px;
  color: #1e1e1e;
}

.TextButton > h3 > span {
  color: #ea5256
}

@media screen and (max-width: 500px) {
  .TextButton > h3 {
    font-size: 20px;
  }
}
</style>
