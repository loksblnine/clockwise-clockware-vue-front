<template>
  <div>
    <div class="image1x">
      <img src="@/components/Content/assets/decorative-routes-thing.png">
    </div>
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
  name: "decorativeRoutesThingMiddle"
}
</script>

<style scoped>
.image1x {
  display: none;
}

.image2x {
  display: none;
}

.image3x {
  position: absolute;
  left: 0;
  bottom: 200px;
  z-index: -100;
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
}

@media screen and (max-width: 1025px) {
  .image1x {
    display: none;
  }
  .image2x {
    display: flex;
    position: absolute;
    left: 0;
    opacity: 0.5;
    bottom: 200px;
    z-index: -100;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
  }
  .image3x {
    display: none;
  }
}

@media screen and (max-width: 500px) {
  .image1x {
    opacity: 0.5;
    display: flex;
    position: absolute;
    left: 0;
    bottom: 480px;
    z-index: -100;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
  }

  .image2x {
    display: none;
  }

  .image3x {
    display: none;
  }
}
</style>
