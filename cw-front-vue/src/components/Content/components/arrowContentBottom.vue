<template>
  <div>
    <div class="image1x">
      <p>Scroll for more information</p>
      <img src="@/components/Content/assets/scroll-down-arrow.png">
    </div>
    <div class="image2x">
      <p>Scroll for more information</p>
      <img src="@/components/Content/assets/scroll-down-arrow@2x.png">
    </div>
    <div class="image3x">
      <p>Scroll for more information</p>
      <img src="@/components/Content/assets/scroll-down-arrow@3x.png">
    </div>
  </div>
</template>

<script>
export default {
  name: "arrowContentBottom"
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
  position: fixed;
  left: 2vw;
  top: 50%;
  z-index: -80;
  display: table;
}

.image3x > p {
  transform: rotate(-90deg);
  margin-bottom: 100px;
}

@media screen and (max-width: 1025px) {
  .image1x {
    display: none;
  }

  .image2x {
    position: fixed;
    left: -50px;
    top: 50%;
    z-index: -80;
    display: table;
  }

  .image2x > p {
    transform: rotate(-90deg);
    margin-bottom: 100px;
  }

  .image3x {
    display: none;
  }
}

@media screen and (max-width: 500px) {
  .image1x {
    display: none;
  }

  .image2x {
    display: none;
  }

  .image3x {
    display: none;
  }
}
</style>
