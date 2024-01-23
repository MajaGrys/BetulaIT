<script setup>
import Navigation from './components/Navigation.vue';
import Home from './components/Home.vue';
import Services from './components/Services.vue';
import About from './components/About.vue';
import Contact from './components/Contact.vue';

import AOS from "aos";
import 'aos/dist/aos.css';
AOS.init({
  delay: 200,
  duration: 1000,
  once: true,
});
</script>

<template>
  <Navigation />

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
  --background:#F8F8FF;
  --purple: #30287b;
  --orange: #db5204;
  --orange-light: #f27a35;
  --black: #2b2928;
  --main-font: 'Montserrat', sans-serif;
  --logo-font: 'Bebas Neue', sans-serif;
}

*, *::before, *::after {
 	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

html {
  background-color: var(--background);
  font-family: var(--main-font);
  font-size: large;
  color: var(--black);
  scroll-behavior: smooth;
  cursor: default;
}

.section-content {
  max-width: 80vw;
  margin: auto;
}

h2 {
  text-align: center;
  font-size: 3rem;
  padding: 80px 0px;
}

h2:not(#kontakt > h2) {
  color: var(--orange);
}
  
@media screen and (min-width: 400px) {
  h2:not(#kontakt > h2) {
    color: var(--black);
  }
  
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
</style>