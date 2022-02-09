<template>
  <div class="Issue">
    <h3>Have you experienced any of these issues?</h3>
  </div>
</template>

<script>
export default {
  name: "Issue"
}
</script>

<style scoped>
.Issue {
  margin: 168px 253px 168px 28px;
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

@media screen and (max-width: 900px) {
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
    margin-left: 10px;
    margin-top: 50px;
  }

  .Issue > h3 {
    margin-bottom: 0;
    width: 350px;
    height: 80px;
    font-size: 15px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: -0.38px;
  }
}
</style>