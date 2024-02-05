<script setup>
import company from '../images/handshake.png';

const servicesList = [
  {name: "Obsługa informatyczna firm", img: company},
  {name: "Serwis urządzeń", img: company},
  {name: "Systemy alarmowe", img: company},
  {name: "Sprzedaż elektroniki", img: company},
];
</script>

<template>
  <section id="oferta">
    <h2 data-aos="zoom-in-up">Oferta</h2>
    <ul class="section-content">
      <li class="card" v-for="service in servicesList" data-aos="zoom-in-up">
        <img :src=service.img alt="" />
        <h3>{{service.name}}</h3>
      </li>
    </ul>
  </section>
</template>

<style scoped>
ul {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 50px 30px;
  list-style: none;
}

.card {
  display: flex;
  align-items: center;
  text-align: center;
  flex-direction: column;
  gap: 20px;
  border-left: 2px solid var(--orange);
  border-radius: 10px;
  padding: 30px;
  margin-bottom: 100px;
  background-color: #f3f3fa;

  img {
    background-color: var(--orange);
    max-width: 80px;
    padding: 10px;
    border-radius: 50px;
  }

  h3 {
    font-weight: 500;
  }

  &:hover {
    transform: scale(1.05);
    cursor: pointer;
    transition: 0.5s;
}}
</style>
