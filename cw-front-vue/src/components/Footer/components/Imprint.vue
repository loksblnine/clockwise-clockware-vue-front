<template>
<span class="Im">
      Data Protection / Imprint
    </span>
</template>

<script>
export default {
  name: "Imprint"
}
</script>

<style scoped>

.Im {
  margin-right: 310px;
  margin-top: 40px;
  width: 200px;
  height: 20px;
  font-family: OpenSans, serif;
  font-size: 13px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.72px;
  text-align: center;
  color: #fff;
}

@media screen and (max-width: 800px) {
  .Im {
    margin-right: 205px;
  }
}

@media screen and (max-width: 600px) {
  .Im {
    margin-right: 25px;
  }
}

@media screen and (min-width: 150px) and (max-width: 300px) {
  .Im {
    margin: 34px 0 42px 0;
    width: 150px;
    height: 20px;
    font-size: 8px;
    font-weight: 600;
    letter-spacing: 0.72px;
  }
}

@media screen and (max-width: 150px) {
  .Im {
    margin: 30px 0 42px 0;
    width: 75px;
    height: 20px;
    font-size: 6px;
    font-weight: 400;
    letter-spacing: 0.12px;
  }
}
</style>
