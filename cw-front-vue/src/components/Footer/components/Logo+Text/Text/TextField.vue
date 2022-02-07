<template>
  <div class="TextField">
    <Clockwise/>
    <Software/>
  </div>
</template>

<script>
import Software from "@/components/Footer/components/Logo+Text/Text/Software";
import Clockwise from "@/components/Footer/components/Logo+Text/Text/Clockwise";

export default {
  name: "Text",
  components: {
    Clockwise,
    Software
  }
}
</script>

<style scoped>
.TextField {
  display: flex;
  flex-direction: column;
  margin-left: 4px;
}
</style>
