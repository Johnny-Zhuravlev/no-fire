<template>
  <div class="container-fluid">
    <div v-if="product" class="container py-5">
      <div class="hero-container">
        <div class="hero__img rounded-lg overflow-hidden">
          <img
            :src="require(`@/assets/img/${product.image}`)"
            :alt="product.description"
            class="image"
          >
        </div>
        <div class="info-box p-3 lg-p-4 rounded-lg">
          <h1>{{ product.title }}</h1>
          <p class="snippet">
            {{ product.subtitle }}
          </p>
          <RentModal :product="product" />
        </div>
      </div>
      <div class="whats-included-container">
        <div class="included-container">
          <h6>Super Effective</h6>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
            dolorem.
          </p>
        </div>
        <div class="included-container">
          <h6>Clean & Tidy</h6>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
            dolorem.
          </p>
        </div>
        <div class="included-container">
          <h6>Cancel Anytime</h6>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
            dolorem.
          </p>
        </div>
        <div class="included-container">
          <h6>Satisfaction Guaranteed</h6>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
            dolorem.
          </p>
        </div>
      </div>
      <div class="description-container">
        <p>
          {{ product.description }}
        </p>
      </div>
      <ReviewsBlock />
    </div>
    <div v-else class="container empty">
      <PageNotFound />
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    product () {
      return this.$store.getters.getProductById(this.$route.params.id)
    }
  }
}
</script>

<style scoped>
.hero-container {
  display: flex;
  justify-content: space-between;
}
.hero__img {
  width: 59%;
  height: 25rem;
}
.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.info-box {
  width: 39%;
  background-color: rgba(207, 201, 201, 0.322);

}
.whats-included-container {
  border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
}
.description-container {
  border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
  padding-bottom: 2rem;
  margin-bottom: 2rem;
}
.included-container {
  margin-top: 1.5rem;
}
h1 {
  font-size: 1.75rem;
}
h6 {
  font-size: 1.15rem;
  font-weight: 400;
}
p {
  color: grey;
}
.snippet {
  color: rgba(0, 0, 0, 0.774);
  margin-top: 1rem;
}
button {
  width: 100%;
  border: none;
  padding: 0.5rem;
  color: white;
  font-weight: 700;
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  font-weight: 700;
  transition: 0.5s;
}
.description-container {
  padding: 3rem 0;
  color: grey;
}
.description-container p {
  margin: 0;
}
.empty {
  padding: 10rem 0;
}

/* media queries */
@media (max-width: 991px) {
  .container-fluid {
    padding: 0 40px;
  }
  .container {
    max-width: 100% !important;
    padding: 0;
  }
  .hero-container {
    gap: 20px;
  }
  .hero__img {
    width: 55%;
  }
  .info-box {
    width: 45%;
  }
}
@media (max-width: 768px) {
  .container-fluid {
    padding: 0 calc(40 * 100% / 768);
  }
  .hero__img {
    width: 53%;
    height: 20rem;
  }
  .info-box h1 {
    font-size: 24px;
    line-height: 28px;
  }
}
@media (max-width: 640px) {
  .hero-container {
    flex-wrap: wrap;
  }
  .hero__img {
    width: 100%;
  }
  .info-box {
    width: 100%;
  }
  .info-box h1 {
    font-size: 24px;
    line-height: 28px;
  }
  .description-container {
    padding: 2rem 0;
  }
}
@media (max-width: 432px) {
  .hero__img {
    height: 15rem;
  }
  .info-box h1 {
    font-size: 20px;
  }
  .included-container:not(:first-child) {
    margin: 1rem 0 0;
  }
  h6 {
    margin: 0 0 5px;
  }
  p {
    line-height: 20px;
  }
  .description-container {
    padding: 1.5rem 0;
  }
}
@media (max-width: 375px) {
  h6 {
    font-size: 16px;
  }
  p {
    font-size: 14px;
  }
}
@media (max-width: 360px) {
  .description-container {
    padding: 1rem 0;
  }
}
</style>
