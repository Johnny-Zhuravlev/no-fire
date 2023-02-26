<template>
  <NuxtLink
    :to="`/products/${card.id}`"
    class="card-fe p-0 mb-3 rounded-lg overflow-hidden cursor-pointer"
  >
    <img :src="require(`@/assets/img/${card.image || 'fe1.jpg'}`)" alt="Fire extinguisher">
  </NuxtLink>
</template>

<script>
export default {
  name: 'LargeCard',
  props: {
    card: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.card-fe {
  width: 24%;
  height: 12.5rem;
}
.card-fe img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
