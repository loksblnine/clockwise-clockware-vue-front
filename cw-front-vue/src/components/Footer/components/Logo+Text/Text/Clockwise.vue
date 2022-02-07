<template>
  <div>
    <span class="CLOCKWISE">
    CLOCKWISE
    </span>
  </div>
</template>

<script>
export default {
  name: "Clockwise"
}
</script>

<style scoped>
@media screen and (min-width: 300px) {
  .CLOCKWISE {
    width: 80px;
    height: 16px;
    margin: 40px 0 48px 0;
    text-align: left;
    font-family: Catamaran, Catamaran, serif;
    font-size: 10px;
    font-weight: 900;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: 0.08px;
    color: #fff;
  }
}

@media screen and (min-width: 150px) and (max-width: 300px) {
  .CLOCKWISE {
    width: 50px;
    height: 12px;
    margin: 0 0 35px 0;
    text-align: left;
    font-family: Catamaran, Catamaran, serif;
    font-size: 8px;
    font-weight: 900;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: 0.08px;
    color: #fff;
  }
}

@media screen and (max-width: 150px) {
  .CLOCKWISE {
    width: 50px;
    height: 12px;
    margin: 0 10px 35px 0;
    text-align: left;
    font-family: Catamaran, Catamaran, serif;
    font-size: 7px;
    font-weight: 800;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: 0.08px;
    color: #fff;
  }
}
</style>
