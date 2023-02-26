<template>
  <div>
    <b-button id="show-btn" @click="showModal">
      Rent
    </b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="calendar">
        <div class="calender__txt">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, hic.
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis consequatur voluptates qui at illo? Expedita?
          </p>
        </div>
        <vc-date-picker
          :value="null"
          color="red"
          is-dark
          is-range
        />
      </div>
      <b-button
        id="show-btn"
        variant="outline-danger"
        class="btn-order"
        @click="() => {
          addItem(product.id)
          hideModal()
        }"
      >
        Order
      </b-button>
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  },
  methods: {
    showModal () {
      this.$refs['my-modal'].show()
    },
    hideModal () {
      this.$refs['my-modal'].hide()
    },
    toggleModal () {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs['my-modal'].toggle('#toggle-btn')
    },
    ...mapMutations(['addItem'])
  }
}
</script>

<style scoped>
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
.calendar {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
.calendar__text {
  padding: 0.5rem;
}
p {
  color: grey;
}
.btn-order {
  margin: 2rem 0 0;
}
</style>
