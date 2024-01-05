<script setup>
import service from '../images/motherboard-885177.jpg';

const listaUsług = [
  "Naprawa komputerów",
  "Obsługa klientów",
  "Zarządzanie stronami WWW",
  "Hosting"
];
</script>

<template>
  <section id="usługi">
    <img :src=service />
    <h2>Usługi informatyczne</h2>
    <ul class="listaUsług">
      <li class="usługa" v-for="usługa in listaUsług">{{usługa}}</li>
    </ul>
  </section>
</template>

<style scoped>
section {
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;

  img {
    height: inherit;
    width: inherit;
    position: absolute;
    object-fit: cover;
    filter: brightness(0.5);
    z-index: -1;
  }
}

h2 {
  color: white;
  font-size: 4rem;
  text-align: center;
  padding: 20px;
}

.listaUsług {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.usługa {
  list-style: none;
  padding: 20px;
  border-radius: 10px;
  background-color: var(--main);
  color: white;
}
</style>
