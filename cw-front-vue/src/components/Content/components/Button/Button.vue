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
  text-align: left;
  font-family: Catamaran, Catamaran, serif;
  font-size: 28px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  object-fit: contain;
  border-radius: 72px;
  background-color: rgba(8, 61, 119);
  color: white;
}
.Button > span { margin: 35px}

@media screen and (max-width: 900px) {
  .Button {
    font-size: 20px;
  }
  .Button > span { margin: 35px}
}
@media screen and (max-width: 500px) {
  .Button {
    font-size: 13px;
  }
  .Button > span { margin: 35px}
}
</style>
