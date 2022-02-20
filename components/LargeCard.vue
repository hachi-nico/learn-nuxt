<template>
  <b-link :to="`/products/${data.id}`" class="card">
    <img :src="require(`@/assets/images/${data.image}`)" alt="" class="image" />
    <h3 class="header">{{ data.header }}</h3>
    <p class="snippet">{{ data.snippet }}</p>
  </b-link>
</template>

<script>
export default {
  props: ["data"],
};
</script>

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.snippet {
  color: grey;
}
</style>
