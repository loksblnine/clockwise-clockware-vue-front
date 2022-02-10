<template>
  <button class="Button">
    <span>{{ msg }}</span>
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    msg: String
  }
}
</script>

<style scoped>
.Button {
  height: 80px;
  min-width: 560px;
  text-align: center;
  font-family: Catamaran;
  font-size: 28px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  object-fit: contain;
  border-radius: 72px;
  background-color: rgba(8, 61, 119, 1);
  box-shadow: 0 5px 2px -2px rgba(65, 111, 162, 0.5);
  color: white;
}
.Button > span { margin: 55px}

@media screen and (max-width: 1025px) {
  .Button {
    font-size: 20px;
    min-width: 360px;
    height: 64px;
  }
  .Button > span { margin: 35px}
}
@media screen and (max-width: 500px) {
  .Button {
    font-size: 13px;
    height: 42px;
    min-width: 240px;
  }
  .Button > span { margin: 35px}
}
</style>
