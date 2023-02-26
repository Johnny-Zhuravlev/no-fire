<template>
  <div class="title-wrapper mb-3">
    <h3 class="font-weight-bold">
      {{ title }}
    </h3>
    <p v-if="text" class="">
      {{ text }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'BaseTitle',
  props: {
    title: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    }
  }
}
</script>
