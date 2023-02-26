<template>
  <div class="container">
    <BaseTitle
      :title="cardsList.title"
      :text="cardsList.subtitle"
    />

    <div class="cards-list d-flex flex-wrap justify-content-between mb-4">
      <LargeCard
        v-for="card in cardsList.cards"
        :key="card.id"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'LargeCardsList',
  props: {
    cardsList: {
      type: Object,
      required: true
    }
  }
}
</script>
