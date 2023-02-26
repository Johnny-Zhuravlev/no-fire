<template>
  <div class="title-wrapper mb-3">
    <h3 class="title font-weight-bold">
      {{ title }}
    </h3>
    <p v-if="text" class="txt">
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

<style scoped>
@media (max-width: 568px) {
  .title {
    font-size: 24px;
  }
}
@media (max-width: 432px) {
  .title {
    font-size: 20px;
  }
  .txt {
    line-height: 20px;
  }
}
@media (max-width: 360px) {
  .title {
    font-size: 18px;
  }
  .txt {
    font-size: 14px;
    line-height: 18px;
  }
}
</style>
