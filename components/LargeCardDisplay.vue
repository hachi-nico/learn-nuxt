<template>
  <div class="container">
    <h4 class="header">{{ data.title }}</h4>
    <p class="snippet">{{ data.snippet }}</p>
    <div class="cards-container">
      <LargeCard
        v-for="item in data.cards"
        :key="item.id"
        :data="item"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ["data"],
};
</script>

<style scoped>
.container {
  margin-top: 2rem;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
}
.snippet {
  color: grey;
  margin-bottom: 1.5rem;
}
.cards-container {
  display: flex;
  justify-content: space-between;
}
</style>
