<template>
  <div class="Achievements">
    <h1>WHAT OUR PARTNERS HAVE ACHIEVED
      WITH CUSTOM TRANSPORT MANAGEMENT
      SOFTWARE
    </h1>
    <Carousel/>
  </div>
</template>

<script>
import Carousel from "@/components/Content/components/Achievements/Carousel";

export default {
  name: "Achievements",
  components: {Carousel}
}
</script>

<style scoped>
.Achievements {
  margin-top: 100px;
}

.Achievements > h1 {
  font-family: Catamaran-Black;
  margin-right: 253px;
  font-size: 35px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: -0.88px;
  text-align: right;
  color: #1e1e1e;
}

@media screen and (max-width: 1025px) {
  .Achievements > h1 {
    margin-left: 165px;
    width: 512px;
    height: 75px;
    font-family: Catamaran-Black;
    font-size: 25px;
    font-weight: 900;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: -0.63px;
    text-align: right;
    color: #1e1e1e;
  }
}

@media screen and (max-width: 500px) {
  .Achievements > h1 {
    font-size: 25px;
    margin: 0 0 100px -5px;
    width: 100%;
    white-space: pre-wrap;
  }
}
</style>
