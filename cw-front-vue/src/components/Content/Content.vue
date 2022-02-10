<template>
  <div>
    <decorativeRoutesThingTop/>
    <decorativeRoutesThingMiddle/>
    <ArrowContentBottom/>
    <Management/>
<!--    <decorativeRoutesThingBottom/>-->
    <Issue/>
    <Benefit/>
    <Achievements/>
    <YourCase/>
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
import YourCase from "@/components/Content/components/YourCase/YourCase";
import Achievements from "@/components/Content/components/Achievements/Achievements";
// import groupDecorCircles from "@/components/Content/components/Benefit/groupDecorCircles";

export default {
  name: "Content",
  components: {
    Achievements,
    YourCase,
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
