<template>
  <div class="py-4">
    <div class="products container">
      <LargeCardsList
        v-for="cardsList of largeCardsList.slice(0, 1)"
        :key="cardsList.title"
        :cards-list="cardsList"
      />
      <SmallCardsList
        v-for="cardsList of smallCardsList"
        :key="cardsList.id"
        :cards-list="cardsList"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '~/assets/data.js'
export default {
  data () {
    return {
      largeCardsList: largeCardSections,
      smallCardsList: smallCardSections
    }
  }
}
</script>

<style scoped>
@media (max-width: 991px) {
  .products.container {
    max-width: 100% !important;
    padding: 0 40px;
  }

  .container {
    max-width: 100% !important;
  }
}
@media (max-width: 991px) {
  .container {
    padding: 0;
  }
}
@media (max-width: 568px) {
  .products.container {
    padding: 0 30px;
  }
}
@media (max-width: 432px) {
  .products.container {
    padding: 0 calc(25 * 100% / 432);
  }
}
</style>
