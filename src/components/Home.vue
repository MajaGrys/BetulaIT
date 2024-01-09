<script setup>
import arrow from '../images/arrow-right-circle.svg';
</script>

<template>
    <section id="home">
        <h1>Usługi informatyczne</h1>
        <a href="#oferta" class="btn">Zobacz ofertę <img :src=arrow /></a>
    </section>
</template>

<style scoped>
section {
  height: 100vh;
  background: url('../images/motherboard-885177.jpg') center no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h1 {
  text-align: center;
  padding: 20px 0px;
  font-size: 1.5rem;
  color: white;
}

@media (min-width: 300px) {
  h1 {
    padding: 20px;
    font-size: 2rem;
  }
}

@media (min-width: 430px) {
  h1 {
    font-size: 3rem;
  }
}

@media (min-width: 600px) {
  h1 {
    font-size: 4rem;
  }
}

.btn {
  text-decoration: none;
  padding-top: 15px;
}

img {
  filter: invert(1);
  height: 22px;
  transform: translateY(4px);
}
</style>