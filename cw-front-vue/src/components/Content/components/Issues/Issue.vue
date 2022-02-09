<template>
  <div class="Issue">
    <h3>Have you experienced any of these issues?</h3>
    <Carousel/>
  </div>
</template>

<script>
import Carousel from "@/components/Content/components/Issues/Carousel";

export default {
  name: "Issue",
  components: {
    Carousel
  }
}
</script>

<style scoped>
.Issue {
  margin: 168px 0px 168px 28px;
}

.Issue > h3 {
  width: 903px;
  height: 35px;
  font-family: Catamaran;
  font-size: 35px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: -0.88px;
  text-align: right;
  color: #1e1e1e;
}

@media screen and (max-width: 1010px) {
  .Issue {
    margin-left: 100px;
    margin-top: 100px;
  }

  .Issue > h3 {
    margin-bottom: 0;
    width: 450px;
    height: 80px;
    font-size: 21px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: -0.38px;
  }
}

@media screen and (max-width: 500px) {
  .Issue {
    margin: 0;
    align-items: center;
  }

  .Issue > h3 {
    text-align: center;
    margin-left: 20px;
    margin-bottom: 0;
    width: 300px;
    height: 40px;
    font-size: 17px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: -0.38px;
  }
}
</style>