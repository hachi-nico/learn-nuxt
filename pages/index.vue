<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="item in largeCardSections"
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
  name: "IndexPage",
  data() {
    return {
      largeCardSections,
      smallCardSections,
    };
  },
};
</script>
