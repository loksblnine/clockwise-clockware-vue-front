<template>
  <div class="Management">
    <h3>LOGISTICS MANAGEMENT SOFTWARE DEVELOPMENT</h3>
    <p>
      We solve transportation and stock management problems for Factories, Manufacturers, Carriers, Resellers,
      E-commerce and even more. Any issue can be solved with smart digitalization.</p>
    <Button msg="Request a free consultation"/>
  </div>
</template>

<script>
import Button from "@/components/Content/components/Button/Button";

export default {
  name: "Management",
  components: {Button}
}
</script>

<style scoped>
.Management {
  display: table;
  position: relative;
  margin-left: 250px;
}

.Management > h3 {
  text-align: left;
  width: 710px;
  height: 110px;
  margin: 48px 63px 49px 45px;
  font-family: Catamaran-Black;
  font-size: 55px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: -1.38px;
  color: #1e1e1e;
}

.Management > p {
  text-align: left;
  width: 564px;
  height: 112px;
  margin: 49px 26px 62px 45px;
  opacity: 0.75;
  font-family: OpenSans;
  font-size: 21px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.53px;
  color: #1a1d1a;
}

@media screen and (max-width: 1025px) {
  .Management {
    margin-left: 130px;
  }

  .Management > h3 {
    margin-bottom: 68px;
    width: 452px;
    height: 80px;
    font-size: 35px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: -0.88px;
  }

  .Management > p {
    margin-top: 0;
    width: 452px;
    height: auto;
    font-size: 17px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: -0.43px;

  }
}

@media screen and (max-width: 500px) {
  .Management {
    margin-left: 0;
  }

  .Management > h3 {
    margin-bottom: 0;
    width: 215px;
    height: 56px;
    font-size: 16px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: 0;
  }

  .Management > p {
    margin-top: 0;
    width: auto;
    height: auto;
    font-size: 14px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
  }
}

</style>
