<template>
  <div>
    <decorativeRoutesThingTop/>
    <decorativeRoutesThingMiddle/>
    <ArrowContentBottom/>
    <Management/>
    <!--    <decorativeRoutesThingBottom/>-->
  </div>
</template>

<script>
import decorativeRoutesThingTop from "@/components/Content/components/decorativeRoutesThingTop";
import decorativeRoutesThingMiddle from "@/components/Content/components/decorativeRoutesThingMiddle";
// import decorativeRoutesThingBottom from "@/components/Content/components/decorativeRoutesThingBottom";
import Management from "@/components/Content/components/Managment/Managment";
import ArrowContentBottom from "@/components/Content/components/arrowContentBottom";

export default {
  name: "Content",
  components: {
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
