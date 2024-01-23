<script setup>
import company from '../images/obsługa-informatyczna-firm.webp';
import computer from '../images/naprawa-komputerów.webp';
import recovery from '../images/odzyskiwanie-danych.webp';
import service from '../images/doradztwo.webp';

const servicesList = [
  {name: "Obsługa informatyczna firm", img: company},
  {name: "Naprawa komputerów i laptopów", img: computer},
  {name: "Odzyskiwanie danych", img: recovery},
  {name: "Doradztwo w zakresie informatyki", img: service},
];
</script>

<template>
  <section id="oferta">
    <h2 data-aos="zoom-in-up">Oferta</h2>
    <ul class="section-content">
      <li class="card" v-for="service in servicesList" data-aos="zoom-in-up">
        <img :src=service.img alt="" />
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
    transition: 0.5s;
  }

  p {
    padding: 20px;
    color: white;
    border-radius: 0px 0px 20px 20px;
    background-color: var(--purple);
  }

  &:hover img {
    transform: scale(1.1);
  }
}
</style>
