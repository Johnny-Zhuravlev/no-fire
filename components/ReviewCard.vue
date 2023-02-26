<template>
  <div class="review">
    <div class="review__image rounded-circle overflow-hidden">
      <img :src="review.picture.large" :alt="review.picture.name">
    </div>
    <div class="review__txt">
      <h6>
        {{ review.login.username }}
      </h6>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure id, eius cum magni non ad?
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    review: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.review {
  height: 4rem;
  display: flex;
  margin-top: 1.5rem;
}
.review__img {
  width: 4rem;
  height: 4rem;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.review__txt {
  margin-left: 2rem;
}
p {
  color: grey;
}
</style>
