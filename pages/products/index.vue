<template>
  <div>
    <Navbar />
    <div class="conatiner">
      <LargeCardDisplay
        v-for="item in largeCardSections.slice(0, 1)"
        :key="item.id"
        :data="item"
      />
      <SmallCardDisplay
        v-for="item in smallCardSections"
        :key="item.id"
        :data="item"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCardSections,
      smallCardSections,
    };
  },
};
</script>

<style lang="scss" scoped></style>
