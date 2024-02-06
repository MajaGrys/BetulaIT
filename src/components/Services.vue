<script setup>
import company from '../images/icon-handshake.png';
import computer from '../images/icon-computer.png';
import camera from '../images/icon-security.png';
import keyboard from '../images/icon-keyboard.png';

const servicesList = [
  {name: "Obsługa informatyczna firm", img: company},
  {name: "Serwis urządzeń", img: computer},
  {name: "Systemy alarmowe", img: camera},
  {name: "Sprzedaż elektroniki", img: keyboard},
];
</script>

<template>
  <section id="oferta">
    <h2 data-aos="zoom-in-up">Oferta</h2>
    <ul class="section-content">
      <li class="card" v-for="service in servicesList" data-aos="zoom-in-up">
        <div class="img-wrap"><img :src=service.img alt="" /></div>
        <h3>{{service.name}}</h3>
      </li>
    </ul>
  <div class="companies">
  <div data-aos="zoom-in-up">
    <h4>Świetnie znamy sprzęt tych firm</h4>
    <div class="companies-imgs">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-dell.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-lenovo.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-acer.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-hp.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-asus.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-intel.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-nvidia.png">
      <img src="https://itvip.pl/wp-content/uploads/2022/02/logo-toshiba.png">
    </div>
  </div>
  </div>
  </section>
</template>

<style scoped>
section {
  background-color: var(--background-light);
}

ul {
  display: grid;
  grid-template-columns: 1fr;
  gap: 50px;
}

@media screen and (min-width: 768px) {
  ul {
    grid-template-columns: 1fr 1fr;
  }
}

.card {
  display: flex;
  align-items: center;
  text-align: center;
  flex-direction: column;
  gap: 20px;
  padding: 30px;
  border-left: 2px solid var(--primary);
  background-color: var(--background);
  border-radius: var(--radius);
  transition: var(--transition);

  .img-wrap {
    background-color: var(--primary);
    width: 80px;
    height: 80px;
    padding: 15px;
    border-radius: 100%;

    img {
      width: 50px;
      height: 50px;
    }
  }

  h3 {
    font-weight: 500;
    font-size: x-large;
  }

  &:hover {
    transform: scale(1.05);
    cursor: pointer;
    transition: var(--transition);
}}

@media screen and (min-width: 1200px) {
  .card {
    padding: 50px;
  }
}

.companies {
  margin-top: 80px;
  padding: 100px 20px;
  background-color: var(--background);

  div {
    max-width: 1000px;
    margin: auto;
  }
}


h4 {
  text-align: center;
  font-size: xx-large;
  font-weight: 500;
  margin-bottom: 40px;
}

.companies-imgs {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 50px;
  flex-wrap: wrap;
}
</style>
