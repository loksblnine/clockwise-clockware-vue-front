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
@media screen and (min-width: 300px) {
  .Im {
    margin: 42px 0 42px 0;
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
}

@media screen and (min-width: 150px) and (max-width: 300px) {
  .Im {
    margin: 34px 0 42px 0;
    width: 150px;
    height: 20px;
    font-family: OpenSans, serif;
    font-size: 8px;
    font-weight: 600;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: 0.72px;
    text-align: center;
    color: #fff;

  }
}

@media screen and (max-width: 150px) {
  .Im {
    margin: 30px 0 42px 0;
    width: 75px;
    height: 20px;
    font-family: OpenSans, serif;
    font-size: 6px;
    font-weight: 400;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: 0.12px;
    text-align: center;
    color: #fff;
  }
}
</style>
