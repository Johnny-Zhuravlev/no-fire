<template>
  <div class="reviews">
    <h3 class="reviews__title">
      Customer Reviews
    </h3>
    <div v-if="!$fetchState.pending">
      <ReviewCard
        v-for="review of reviews.results"
        :key="review.login.uiid"
        :review="review"
      />
    </div>
    <div v-else>
      Loading...
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      reviews: []
    }
  },
  async fetch () {
    this.reviews = await fetch(
      'https://randomuser.me/api/?results=7'
    ).then(res => res.json())
  }
}
</script>

<style scoped>
@media (max-width: 768px) {
  .reviews__title {
    font-size: 24px;
    line-height: 28px;
  }
}
@media (max-width: 432px) {
  .reviews__title {
    font-size: 20px;
  }
}
</style>
