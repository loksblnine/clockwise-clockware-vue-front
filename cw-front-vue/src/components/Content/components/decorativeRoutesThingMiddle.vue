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
  right: 0;
  top: 280px;
  z-index: -100;
}

@media screen and (max-width: 1010px) {
  .image1x {
    display: none;
  }

  .image2x {
    display: flex;
    position: absolute;
    right: 0;
    top: 280px;
    z-index: -100;
  }

  .image3x {
    display: none;
  }
}

@media screen and (max-width: 500px) {
  .image1x {
    display: flex;
    position: absolute;
    right: 0;
    top: 280px;
    z-index: -100;
  }

  .image2x {
    display: none;
  }

  .image3x {
    display: none;
  }
}
</style>
