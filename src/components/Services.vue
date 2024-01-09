<script setup>
// import computer from '../images/icons8-laptop-settings.gif';
// import service from '../images/icons8-customer-support.gif';
// import website from '../images/icons8-program.gif';

// import computer from '../images/computer-161501_640.png';
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
  justify-content: center;
  gap: 50px 20px;
  text-align: center;
  list-style: none;
}

img {
  max-height: 300px;
  max-width: 300px;
  display: block;
  margin: 0px auto 20px auto;
}

@media screen and (max-width: 350px) {
  img {
    max-height: 200px;
    max-width: 200px;
  }
}
</style>
