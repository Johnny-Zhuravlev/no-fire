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

<style scoped>
@media (max-width: 991px) {
  .main.container {
    max-width: 90% !important;
  }
  .container {
    max-width: 100%;
  }
}
@media (max-width: 640px) {
  .main.container {
    max-width: 100% !important;
    padding: 0 30px;
  }
  .container {
    padding-right: 0;
    padding-left: 0;
  }
}
@media (max-width: 432px) {
  .main.container {
    padding: 0 calc(25 * 100% / 432);
  }
  .container {
    padding-right: 0;
    padding-left: 0;
  }
}
</style>
