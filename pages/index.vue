<template>
  <div>
    <div class="main container">
      <TheHero />
      <LargeCardsList
        v-for="cardsList of largeCardsList"
        :key="cardsList.id"
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
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  data () {
    return {
      largeCardsList: largeCardSections,
      smallCardsList: smallCardSections
    }
  }
}
</script>
