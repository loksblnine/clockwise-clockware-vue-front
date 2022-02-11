<template>
  <div>
    <decorativeRoutesThingTop/>
    <decorativeRoutesThingMiddle/>
    <ArrowContentBottom/>
    <Management/>
    <Issue/>
    <Benefit/>
    <OurAdvantages/>
    <Achievements/>
    <YourCase/>
  </div>
</template>

<script>
import decorativeRoutesThingTop from "@/components/Content/components/decorativeRoutesThingTop";
import decorativeRoutesThingMiddle from "@/components/Content/components/decorativeRoutesThingMiddle";
import Management from "@/components/Content/components/Managment/Managment";
import ArrowContentBottom from "@/components/Content/components/arrowContentBottom";
import Issue from "./components/Issues/Issue";
import Benefit from "@/components/Content/components/Benefit/Benefit";
import YourCase from "@/components/Content/components/YourCase/YourCase";
import Achievements from "@/components/Content/components/Achievements/Achievements";
import OurAdvantages from "@/components/Content/components/Advantages/OurAdvantages";

export default {
  name: "Content",
  components: {
    OurAdvantages,
    Achievements,
    YourCase,
    Benefit,
    Issue,
    ArrowContentBottom,
    Management,
    decorativeRoutesThingTop,
    decorativeRoutesThingMiddle,
  }

}
</script>

<style scoped>

</style>
