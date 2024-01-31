<script setup>
import arrow from '../images/arrow-right-circle.svg';
</script>

<template>
  <section id="home">
      <h1>Usługi informatyczne</h1>
      <a href="#oferta" class="btn">Zobacz ofertę <img :src=arrow alt="" /></a>
  </section>
</template>

<style scoped>
section {
  height: 100vh;
  background: url('../images/motherboard-885177.webp') center no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h1 {
  text-align: center;
  padding: 20px 20px 50px 20px;
  font-size: 1.5rem;
  color: white;
}

@media (min-width: 300px) {
  h1 {
    font-size: 2rem;
  }
}

@media (min-width: 430px) {
  h1 {
    font-size: 3rem;
  }
}

@media (min-width: 600px) and (min-height: 400px) {
  h1 {
    font-size: 4rem;
  }
}

.btn {
  color: white;
  background-color: var(--orange);
  padding: 15px 20px 20px 20px;
  border-radius: 30px;
  text-decoration: none;
  transition: 0.5s;

  &:hover, &:focus {
    transform: scale(1.1);
  }
}

img {
  filter: invert(1);
  height: 22px;
  transform: translateY(4px);
}
</style>