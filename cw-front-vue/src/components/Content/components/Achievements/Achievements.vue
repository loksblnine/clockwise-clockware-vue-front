<template>
  <div class="Achievements">
    <h1>WHAT OUR PARTNERS HAVE ACHIEVED <br>
      WITH CUSTOM TRANSPORT MANAGEMENT<br>
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
    margin: 0 50px;
  }
}

@media screen and (max-width: 500px) {
  .Achievements > h1 {
    margin-right: 20px;
    font-size: 20px;
    width: auto;
  }
}
</style>
