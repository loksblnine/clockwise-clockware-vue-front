<template>
  <div class="OurAdvantages">
    <Advantages/>
    <Feedback/>
  </div>
</template>

<script>
import Feedback from "@/components/Content/components/Advantages/Feedback";
import Advantages from "@/components/Content/components/Advantages/Advantages";

export default {
  name: "OurAdvantages",
  components: {
    Feedback,
    Advantages
  }

}
</script>

<style scoped>
.OurAdvantages {
  display: flex;
  flex-direction: row;
}

@media screen and (max-width: 1025px) {

  .OurAdvantages {
    flex-direction: column;
  }
}

@media screen and (max-width: 500px) {

}
</style>
