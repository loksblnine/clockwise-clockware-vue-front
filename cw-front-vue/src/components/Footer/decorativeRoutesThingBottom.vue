<template>
  <div>
    <div class="image2x">
      <img src="@/components/Content/assets/decorative-routes-thing@2x.png">
    </div>
    <div class="image3x">
      <img src="@/components/Content/assets/decorative-routes-thing@3x.png">
    </div>
  </div>
</template>

<script>
export default {
  name: "decorativeRoutesThingMiddle",
}
</script>

<style scoped>
.image2x {
  display: none;
}

.image3x {
  position: absolute;
  left: 0;
  background: white;
  opacity: 1;
  bottom: 200px;
  z-index: -10;
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
}

@media screen and (max-width: 1025px) {
  .image2x {
    display: flex;
    position: absolute;
    background: white;
    left: 0;
    opacity: 1;
    bottom: 200px;
    z-index: -10;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
  }
  .image3x {
    display: none;
  }
}

@media screen and (max-width: 500px) {
  .image2x {
    display: none;
  }

  .image3x {
    display: none;
  }
}

</style>
