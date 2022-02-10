<template>
  <div>
    <decorativeRoutesThingTop/>
    <decorativeRoutesThingMiddle/>
    <ArrowContentBottom/>
    <Management/>
<!--    <decorativeRoutesThingBottom/>-->
    <Issue/>
    <Benefit/>
  </div>
</template>

<script>
import decorativeRoutesThingTop from "@/components/Content/components/decorativeRoutesThingTop";
import decorativeRoutesThingMiddle from "@/components/Content/components/decorativeRoutesThingMiddle";
// import decorativeRoutesThingBottom from "@/components/Content/components/decorativeRoutesThingBottom";
import Management from "@/components/Content/components/Managment/Managment";
import ArrowContentBottom from "@/components/Content/components/arrowContentBottom";
import Issue from "./components/Issues/Issue";
import Benefit from "@/components/Content/components/Benefit/Benefit";
// import groupDecorCircles from "@/components/Content/components/Benefit/groupDecorCircles";

export default {
  name: "Content",
  components: {
    Benefit,
    // groupDecorCircles,
    Issue,
    ArrowContentBottom,
    Management,
    decorativeRoutesThingTop,
    decorativeRoutesThingMiddle,
    // decorativeRoutesThingBottom
  }

}
</script>

<style scoped>

</style>
