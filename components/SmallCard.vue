<template>
  <b-link :to="`/products/${data.id}`" class="card-container" :prefetch="true">
    <img :src="require(`@/assets/images/${data.image}`)" alt="" class="image" />
  </b-link>
</template>

<script>
export default {
  props: ["data"],
};
</script>

<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}

.image {
  width: 100%;
  height: 100%;
}
</style>
