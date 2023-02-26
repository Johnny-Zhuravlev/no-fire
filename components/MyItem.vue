<template>
  <div class="item-container">
    <div class="img-wrapper rounded-lg overflow-hidden">
      <img :src="require(`@/assets/img/${item.image}`)" alt="pic of fe">
    </div>
    <div class="text-container">
      <h4>{{ item.title }}</h4>
      <p>{{ item.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.item-container {
  display: flex;
  margin: 0 0 2rem;
}
.text-container {
  padding: 0 1rem;
}
.img-wrapper {
  width: 17.5rem;
  flex: none;
  height: 11rem;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
p {
  font-size: 0.8rem;
  color: grey;
}
</style>
