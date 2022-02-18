<template>
  <div class="Footer">
    <Imprint/>
    <LogoText/>
    <decorativeRoutesThingBottom/>
  </div>
</template>

<script>
import Imprint from "@/components/Footer/components/Imprint";
import LogoText from "@/components/Footer/components/LogoText";
import decorativeRoutesThingBottom from "@/components/Footer/decorativeRoutesThingBottom";

export default {
  name: "Footer",
  components: {
    LogoText,
    Imprint,
    decorativeRoutesThingBottom
  },

  props: {
    msg: String
  }
}
</script>

<style scoped>
.Footer {
  display: flex;
  position: relative;
  height: 104px;
  bottom: -104px;
  background: #000000;
  justify-content: center;
}

@media screen and (max-width: 300px) {
  .Footer {
    height: 80px;
  }
}
</style>
