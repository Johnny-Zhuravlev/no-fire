<template>
  <b-navbar
    class="navbar navbar-expand-lg padding bg-dark"
    toggleable="lg"
    type="dark"
    variant="info"
  >
    <NuxtLink class="navbar-brand text-white" to="/">
      Noo-fire
    </NuxtLink>
    <b-navbar-toggle target="nav-collapse" />

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="navbar-nav ml-auto">
        <b-nav-item class="nav-item active">
          <NuxtLink
            class="nav-link"
            to="/products"
          >
            Products <span class="sr-only">(current)</span>
          </NuxtLink>
        </b-nav-item>
        <b-nav-item class="nav-item">
          <NuxtLink class="nav-link" to="/my-items">
            My Items
          </NuxtLink>
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {}
</script>

<style scoped>
.nav-link {
  color: #fff !important;
}
</style>
