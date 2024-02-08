<script setup>
import Navigation from './components/Navigation.vue';
import Home from './components/Home.vue';
import Services from './components/Services.vue';
import About from './components/About.vue';
import Contact from './components/Contact.vue';

import AOS from "aos";
import 'aos/dist/aos.css';
AOS.init({
  duration: 1000,
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
  --background:#191923;
  --background-light: #2b2b39;
  --font-color: #ffffff;
  --primary: #006CF0;
  --main-font: 'Montserrat', sans-serif;
  --logo-font: 'Bebas Neue', sans-serif;
  --transition: 0.5s;
  --radius: 20px;
}

*, *::before, *::after {
 	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

html {
  background-color: var(--background);
  font-family: var(--main-font);
  color: var(--font-color);
  font-size: large;
  scroll-behavior: smooth;
  cursor: default;
}

.section-content {
  max-width: 70vw;
  margin: auto;
}

h2 {
  text-align: center;
  font-size: 2.5rem;
  padding: 80px 0px;
}

h2::before, h2::after {
  content: "";
  display: inline-block;
  width: 10vw;
  max-width: 160px;
  height: 3px;
  margin: 15px 10px;
  background-color: var(--primary);
}
  
@media screen and (min-width: 400px) {
  h2 {
    font-size: 3rem;
  }

  h2::before, h2::after {
    width: 15vw;
    margin: 15px;
  }
}
</style>