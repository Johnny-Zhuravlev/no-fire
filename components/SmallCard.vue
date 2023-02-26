<template>
  <NuxtLink
    :to="`/products/${card.id}`"
    class="card-fe p-0 rounded-lg overflow-hidden cursor-pointer"
  >
    <img
      :src="require(`@/assets/img/${card.image || 'fe1.jpg'}`)"
      alt="Fire extinguisher"
      loading="lazy"
    >
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
  margin: 0 0 1rem;
}
.card-fe img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* media queries */
@media (max-width: 1200px) {
  .card-fe {
    height: 10rem;
  }
}
@media (max-width: 640px) {
  .card-fe {
    width: 31.5%;
  }
}
@media (max-width: 568px) {
  .card-fe {
    width: 48.5%;
    height: auto;
    margin: 0 0 .75rem;
  }
}
@media (max-width: 432px) {
  .card-fe {
    height: 10rem;
  }
}
@media (max-width: 375px) {
  .card-fe {
    height: 8rem;
    margin: 0 0 .5rem;
  }
}
</style>
