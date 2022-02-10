<template>
  <div class="Footer">
    <Imprint/>
    <LogoText/>
    <decorativeRoutesThingBottom/>
  </div>
</template>

<script>
import Imprint from "@/components/Footer/components/Imprint";
import LogoText from "@/components/Footer/components/Logo+Text/LogoText";
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
  left: 0;
  position: relative;
  height: 104px;
  bottom: -104px;
  background: #1e1e1e;
  width: 100%;
  flex-direction: row;
  justify-content: space-around;
}

@media screen and (max-width: 300px) {
  .Footer {
    height: 80px;
  }
}
</style>
