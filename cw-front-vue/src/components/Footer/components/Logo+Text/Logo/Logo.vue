<template>
  <div class="Shape"></div>
</template>

<script>
export default {
  name: "Logo"
}
</script>

<style scoped>
@media screen and (min-width: 300px) {
  .Shape {
    margin-top: 4px;
    width: 23.8px;
    height: 23.8px;
    padding: 3px 3px 3px 3px;
    background-color: #fff;
  }
}

@media screen and (max-width: 300px) {
  .Shape {
    margin-top: 8px;
    width: 14px;
    height: 14px;
    padding: 3px 3px 3px 3px;
    background-color: #fff;
  }
}
</style>
