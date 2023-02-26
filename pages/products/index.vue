<template>
  <div class="py-4">
    <div class="container">
      <LargeCardsList
        v-for="cardsList of largeCardsList.slice(0, 1)"
        :key="cardsList"
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
