<template>
  <div class="Benefit">
    <groupDecorCircles/>
    <TextButton/>
  </div>
</template>

<script>
import groupDecorCircles from "@/components/Content/components/Benefit/groupDecorCircles";
import TextButton from "@/components/Content/components/Benefit/TextButton";

export default {
  name: "Benefit",
  components: {
    groupDecorCircles,
    TextButton
  }

}
</script>
