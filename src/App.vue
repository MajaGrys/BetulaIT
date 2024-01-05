<script setup>
import Usługi from './components/Usługi.vue';
import ONas from './components/ONas.vue';
import Kontakt from './components/Kontakt.vue';
</script>

<template>
  <nav>
    <a href="#" id="logo">Betula IT</a>
    <div class="links">
      <a href="#usługi">Usługi</a>
      <a href="#o-nas">O nas</a>
      <a href="#">Kontakt</a>
    </div>
    <button id="menu">Menu</button>
  </nav>

  <main>
    <Usługi />
    <ONas />
    <Kontakt />
  </main>
</template>

<style>
/* @import url('https://fonts.googleapis.com/css2?family=Dosis:wght@300&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Tektur&display=swap');

:root {
  --main: #003566;
  --secondary: #e76f51;
  --logo: #e76f51;
  --logo-font: 'Tektur', sans-serif;
  /* 'Dosis', sans-serif; */
  --nav-background: white;
}

*, *::before, *::after {
 	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

html {
  scroll-behavior: smooth;
  cursor: default;
}

nav {
  position: fixed;
  z-index: 100;
  width: 100%;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--nav-background);
  box-shadow: 0px 1px 10px #242424;
}

#logo {
  font-size: 2.5rem;
  font-family: var(--logo-font);
  color: var(--logo);
  text-decoration: none;
}

.links {
  display: none;

  a {
    padding: 0 10px;
    color: var(--main);
    text-decoration: none;
    transition: 0.5s;

    &:hover {
      color: var(--secondary);
    }
  }
}

#menu {
  padding: 15px;
  border-radius: 10px;
  border: 1px solid black;
}

@media (min-width: 620px) {
  .links a {
    padding: 0 20px;
  }
}

@media (min-width: 520px) {
  #menu {
    display: none;
  }

  .links {
    display: flex;
  }
}
</style>
