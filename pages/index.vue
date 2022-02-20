<template>
  <div>
    <Navbar />
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="item in largeCardItem"
        :key="item.id"
        :data="item"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections } from "@/assets/data.js";
export default {
  name: "IndexPage",
  data() {
    return {
      largeCardItem: largeCardSections,
    };
  },
};
</script>
