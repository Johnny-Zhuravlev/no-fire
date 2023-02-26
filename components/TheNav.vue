<template>
  <nav class="navbar navbar-expand-lg padding bg-dark">
    <NuxtLink class="navbar-brand text-white" to="/">
      Noo-fire
    </NuxtLink>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>

    <div id="navbarSupportedContent" class="collapse navbar-collapse">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item active">
          <NuxtLink
            class="nav-link"
            to="/products"
          >
            Products <span class="sr-only">(current)</span>
          </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink class="nav-link" to="/my-items">
            My Items
          </NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {}
</script>

<style scoped>
.nav-link {
  color: #fff !important;
}
</style>
