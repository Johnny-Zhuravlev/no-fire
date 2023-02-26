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
        loading="lazy"
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
  width: 45%;
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

/* media queries */
@media (max-width: 1200px) {
  .hero__title {
    font-size: 4rem;
  }
  .hero__img {
    width: 40%;
  }
}
@media (max-width: 991px) {
  .hero {
    align-items: center;
  }
  .txt-content {
    margin: 0;
  }
  .hero__title {
    font-size: 3rem;
  }
  .hero__img {
    margin: 0;
  }
}
@media (max-width: 768px) {
  .hero {
    align-items: flex-start;
  }
  .txt-content {
    width: 65%;
  }
  .hero__title {
    font-size: 2.75rem;
  }
  .hero__img {
    width: 35%;
  }
}
@media (max-width: 640px) {
  .txt-content {
    width: 80%;
  }
  .hero__img {
    width: 20%;
    position: absolute;
    top: 5rem;
    right: 0;
  }
  .hero__btn {
    width: 15rem;
  }
}
@media (max-width: 568px) {
  .txt-content {
    width: 100%;
  }
  .hero__title {
    font-size: 2.5rem;
  }
  .hero__img {
    display: none;
  }
}
@media (max-width: 432px) {
  .hero.container {
    padding: 3rem 0;
  }
  .txt-content {
    text-align: center;
  }
  .hero__title {
    font-size: 2rem;
  }
  .btn {
    width: unset;
  }
  .hero__btn {
    width: 12rem;
    padding: .8rem 1.5rem;
  }
}
@media (max-width: 360px) {
  .hero__title {
    font-size: 1.5rem;
  }
  .hero__description {
    font-size: 13px;
    line-height: 20px;
  }
  .hero__btn {
    width: 10rem;
    font-size: 0.85rem;
  }
}
</style>
