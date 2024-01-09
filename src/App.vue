<script setup>
import Home from './components/Home.vue';
import Services from './components/Services.vue';
import About from './components/About.vue';
import Contact from './components/Contact.vue';
import menu from './images/menu.svg';

// const navLinks = [
//   {url: '#home', name: 'Strona główna'},
// ]
// {{navLinks[0].url}}

const mobileNavToggle = () => {
  console.log('hi')
}
</script>

<template>
  <nav>
    <a href="#" id="logo"><svg xmlns="http://www.w3.org/2000/svg" height="34" viewBox="0 0 640 512"><path fill="#f35b04" d="M384 96V320H64L64 96H384zM64 32C28.7 32 0 60.7 0 96V320c0 35.3 28.7 64 64 64H181.3l-10.7 32H96c-17.7 0-32 14.3-32 32s14.3 32 32 32H352c17.7 0 32-14.3 32-32s-14.3-32-32-32H277.3l-10.7-32H384c35.3 0 64-28.7 64-64V96c0-35.3-28.7-64-64-64H64zm464 0c-26.5 0-48 21.5-48 48V432c0 26.5 21.5 48 48 48h64c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48H528zm16 64h32c8.8 0 16 7.2 16 16s-7.2 16-16 16H544c-8.8 0-16-7.2-16-16s7.2-16 16-16zm-16 80c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16s-7.2 16-16 16H544c-8.8 0-16-7.2-16-16zm32 160a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"/></svg>Betula IT</a>

    <div class="nav-links">
      <a href="#">Strona główna</a>
      <a href="#oferta">Oferta</a>
      <a href="#o-nas">O nas</a>
      <a href="#kontakt">Kontakt</a>
    </div>

    <button class="btn menu-btn" @click="mobileNavToggle"><img :src=menu></button>
  </nav>

  <main>
    <Home />
    <Services />
    <About />
    <Contact />
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Montserrat&display=swap');

:root {
  --purple: #3d348b;
  --purple-light: #7678ed;
  --orange: #f35b04;
  --orange-light: #f27a35;
  --black: #171615;
  --beige: #f4f3ee;
  --nav-background: #ffffff;
  --main-font: 'Montserrat', sans-serif;
  --logo-font: 'Bebas Neue', sans-serif;
}

*, *::before, *::after {
 	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

html {
  font-family: var(--main-font);
  font-size: large;
  color: var(--black);
  scroll-behavior: smooth;
  cursor: default;
}

.section-content {
  padding: 80px 20px;
  max-width: 80vw;
  margin: auto;
}

h2 {
  text-align: center;
  font-size: 3rem;
  padding-top: 80px;
}

@media screen and (min-width: 310px) and (max-width: 400px) {
  h2::before, h2::after {
    content: "·";
    margin: 20px;
    color: var(--orange-light);
  }
}

@media screen and (min-width: 400px) {
  h2::before, h2::after {
    content: "";
    display: inline-block;
    width: 15vw;
    max-width: 160px;
    height: 3px;
    margin: 15px;
    background-color: var(--orange-light);
  }
}

.btn {
  color: white;
  background-color: var(--orange);
  padding: 20px;
  border: none;
  border-radius: 30px;
  transition: 0.5s;
  cursor: pointer;

  &:hover, &:focus {
    background-color: var(--orange-light);
    transform: scale(1.1);
  }
}

.card {
  flex-grow: 1;
  border: 1px solid var(--purple);
  border-radius: 20px;
  padding-top: 20px;
  display: flex;
  flex-direction: column;
  justify-content: end;

  p {
    padding: 20px;
    color: white;
    border-radius: 0px 0px 20px 20px;
    background-color: var(--purple);
  }
}

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

  svg {
    margin-right: 5px;
  }
}

.nav-links {
  display: none;

  a {
    padding: 29px 15px;
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
  padding: 11.5px;
  border-radius: 15px;

  img {
    filter: invert(1);
  }
}

@media (min-width: 655px) {
  .menu-btn {
    display: none;
  }

  .nav-links {
    display: flex;
  }
}

@media (min-width: 740px) {
  .nav-links a {
    padding: 29px 25px;
  }
}
</style>