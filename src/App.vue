<script setup>
import Navigation from './components/Navigation.vue';
import Home from './components/Home.vue';
import Services from './components/Services.vue';
import About from './components/About.vue';
import Contact from './components/Contact.vue';
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
  --purple: #3d348b;
  --purple-light: #9C9CDD;
  --orange: #f35b04;
  --orange-light: #f27a35;
  --black: #2b2928;
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
  max-width: 80vw;
  margin: auto;
}

h2 {
  text-align: center;
  font-size: 3rem;
  padding: 80px 0px;
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
</style>