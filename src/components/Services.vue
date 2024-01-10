<script setup>
import computer from '../images/computer-2851285_1280.png';
import service from '../images/call-center-7040784_640.png';
import website from '../images/computer-908893_1280.png';

const servicesList = [
  {name: "Naprawa komputerów i drukarek", img: computer},
  {name: "Doradztwo w zakresie informatyki", img: service},
  {name: "Zarządzanie stronami WWW", img: website},
];
</script>

<template>
  <section id="oferta">
    <h2>Oferta</h2>
    <ul class="section-content">
      <li class="card" v-for="service in servicesList">
        <img :src=service.img />
        <p>{{service.name}}</p>
      </li>
    </ul>
  </section>
</template>

<style scoped>
ul {
  display: flex;
  flex-wrap: wrap;
  gap: 50px 20px;
  text-align: center;
  list-style: none;
}

.card {
  border: 1px solid var(--purple);
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  justify-content: end;
  flex-grow: 1;

  img {
    width: 80vw;
    max-width: 300px;
    margin: auto;
    padding: 20px;
  }

  p {
    padding: 20px;
    color: white;
    border-radius: 0px 0px 20px 20px;
    background-color: var(--purple);
  }
}
</style>
