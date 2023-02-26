<template>
  <NuxtLink
    :to="`/products/${card.id}`"
    class="card-fe text-decoration-none text-dark"
  >
    <div class="card-fe__img mb-3 rounded-lg overflow-hidden">
      <img :src="require(`@/assets/img/${card.image || 'fe1.jpg'}`)" alt="Fire extinguisher">
    </div>
    <h4 class="card-fe__title">
      {{ card.title }}
    </h4>
    <p class="card-fe__description">
      {{ card.description }}
    </p>
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
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.card-fe__img {
  height: 65%;
}
.card-fe__img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.card-fe__title {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.card-fe__description {
  color: grey;
}
</style>
