<script setup>
import { ref } from 'vue';
import computer from '../images/komputer.webp';
import menu from '../images/menu.svg';

const navLinks = [
  {url: '#home', name: 'Strona główna'},
  {url: '#oferta', name: 'Oferta'},
  {url: '#o-nas', name: 'O nas'},
  {url: '#kontakt', name: 'Kontakt'},
]

const navOpened = ref(false);

const mobileNavToggle = () => {
  window.innerWidth > 695 ? navOpened.value = false : navOpened.value = !navOpened.value
}

window.addEventListener('resize', () => { if (window.innerWidth > 695) { navOpened.value = false } });
</script>

<template>
  <nav>
    <a href="#home" id="logo"><img :src=computer alt="" />Betula IT</a>
    <div class="nav-links" :class="{mobile: navOpened}" @click="mobileNavToggle">
      <a v-for="link in navLinks" :href=link.url>{{link.name}}</a>
    </div>
    <button class="menu-btn" aria-label="Otwórz nawigację" @click="mobileNavToggle"><img :src=menu alt="" /></button>
  </nav>
</template>

<style scoped>
nav {
  position: fixed;
  height: 80px;
  z-index: 100;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--background);
  box-shadow: 0px 1px 10px #41414141;
}

#logo {
  padding: 10.5px 20px;
  font-size: 2.5rem;
  font-family: var(--logo-font);
  color: var(--orange);
  text-decoration: none;

  img {
    height: 40px;
    width: 40px;
    margin-right: 5px;
    transform: translateY(2px);
  }
}

@media screen and (max-width: 290px) {
  #logo img {
    display: none;
  }
}

.nav-links {
  display: none;

  a {
    padding: 29px 20px;
    color: var(--black);
    text-decoration: none;
    transition: 0.5s;

    &:hover, &:focus {
      color: white;
      background-color: var(--orange);
    }
  }
}

.menu-btn {
  margin-right: 20px;
  padding: 8px;
  background-color: var(--orange);
  border: none;
  border-radius: 15px;
  transition: 0.5s;

  &:hover, &:focus {
    background-color: var(--orange-light);
    transform: scale(1.1);
  }

  img {
    height: 35px;
    filter: invert(1);
    transform: translateY(2px);
  }
}

@media screen and (min-width: 695px) {
  .menu-btn {
    display: none;
  }

  .nav-links {
    display: flex;
  }
}

@media screen and (max-width: 695px) {
  .mobile {
    position: fixed;
    top: 80px;
    width: 100%;
    background-color: var(--background);
    box-shadow: 0px 4px 4px #41414141;
    display: flex;
    flex-direction: column;
    animation: 0.5s slideIn ease-out;

    a {
      text-align: center;
      width: 100%;  
    }
  }
}

@keyframes slideIn {
  from { transform: translateY(-100vh) }
  to { transform: translateY(0) }
}

@media screen and (max-height: 380px) {
  .mobile {
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }
}
</style>