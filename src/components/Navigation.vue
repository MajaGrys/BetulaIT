<script setup>
import { ref } from 'vue';
import logo from '../images/betula-logo.jpg';
import menu from '../images/icon-menu.svg';

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
    <a href="#home" id="logo"><img :src=logo alt="" /></a>
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

#logo img {
  height: 60px;
  margin-left: 20px;
}

.nav-links {
  display: none;

  a {
    padding: 29px 20px;
    color: var(--font-color);
    text-decoration: none;
    transition: var(--transition);

    &:hover, &:focus {
      color: white;
      background-color: var(--primary);
    }
  }
}

.menu-btn {
  margin-right: 20px;
  padding: 8px;
  background-color: var(--primary);
  border: none;
  border-radius: 10px;
  transition: var(--transition);

  &:hover, &:focus {
    transform: scale(1.1);
  }

  img {
    height: 35px;
    filter: invert(1);
    transform: translateY(2px);
  }
}

@media screen and (min-width: 700px) {
  .menu-btn {
    display: none;
  }

  .nav-links {
    display: flex;
  }
}

@media screen and (max-width: 700px) {
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