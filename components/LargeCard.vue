<template>
  <NuxtLink
    :to="`/products/${card.id}`"
    class="card-fe text-decoration-none text-dark"
  >
    <div class="card-fe__img rounded-lg overflow-hidden">
      <img
        :src="require(`@/assets/img/${card.image || 'fe1.jpg'}`)"
        alt="Fire extinguisher"
        loading="lazy"
      >
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
  margin: 0 0 1rem;
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

/* media queries */
@media (max-width: 1200px) {
  .card-fe__img {
    height: 50%;
  }
}
@media (max-width: 768px) {
  .card-fe__img {
    height: 45%;
  }
}
@media (max-width: 640px) {
  .card-fe {
    width: 47%;
  }
}
@media (max-width: 432px) {
  .card-fe {
    width: 100%;
    height: fit-content;
    margin: 0 0 2rem;
  }
  .card-fe__img {
    height: 75%;
  }
  .card-fe__description {
    margin: 0;
  }
}
@media (max-width: 360px) {
  .card-fe {
    margin: 0 0 1.5rem;
  }
  .card-fe__img {
    margin: 0 0 .55rem;
  }
  .card-fe__title {
    font-size: 16px;
  }
  .card-fe__description {
    font-size: 14px;
    line-height: 20px;
  }
}
</style>
