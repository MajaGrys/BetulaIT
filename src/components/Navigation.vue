<script setup>
import computer from '../images/icons8-computer-100.png';
import menu from '../images/menu.svg';

const navLinks = [
  {url: '#', name: 'Strona główna'},
  {url: '#oferta', name: 'Oferta'},
  {url: '#o-nas', name: 'O nas'},
  {url: '#kontakt', name: 'Kontakt'},
]

const mobileNavToggle = () => {
  console.log('hi')
}
</script>

<template>
  <nav>
    <a href="#" id="logo"><img :src=computer />Betula IT</a>
    <div class="nav-links">
      <a v-for="link in navLinks" :href=link.url>{{link.name}}</a>
    </div>
    <button class="btn menu-btn" @click="mobileNavToggle"><img :src=menu /></button>
  </nav>
</template>

<style scoped>
nav {
  position: fixed;
  z-index: 100;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--nav-background);
  box-shadow: 0px 1px 10px #41414141;
}

#logo {
  padding: 10.5px 20px;
  font-size: 2.5rem;
  font-family: var(--logo-font);
  color: var(--orange);
  text-decoration: none;

  img {
    max-height: 40px;
    margin-right: 5px;
    transform: translateY(2px);
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
  border-radius: 15px;

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
</style>