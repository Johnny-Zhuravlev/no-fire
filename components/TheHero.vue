<template>
  <div class="hero container">
    <div class="txt-content">
      <h1 class="hero__title">
        Find your Fire Extinguisher
      </h1>
      <p class="hero__description">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Porro vel
        magni corporis illo, earum culpa reiciendis, quod officiis obcaecati ex
        hic nisi asperiores autem dolorem?
      </p>
      <button class="hero__btn btn">
        Start Looking
      </button>
    </div>

    <div class="hero__img">
      <img
        src="~/assets/svg/hero_img.svg"
        alt="image of fire extinguisher"
      >
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.hero {
  position: relative;
  display: flex;
  padding: 5rem 0;
  align-items: flex-start;
  justify-content: space-between;
}
.txt-content {
  width: 50%;
  margin-top: 4rem;
}
.hero__title {
  font-weight: 900;
  font-size: 5rem;
}
.hero__txt {
  color: grey;
  font-size: 1.25rem;
}
.hero__img {
  width: 27.5rem;
  margin-top: 2rem;
}
.hero__img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.overlay {
  background: rgba(0, 0, 0, 0);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
.hero__btn {
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  width: 20rem;
  font-weight: 700;
  transition: 0.5s;
}
.hero__btn:hover {
  width: 21.5rem;
}
@media (max-width: 500px) {
  .hero {
    height: 40vh;
  }
}
</style>
