<script setup>
import building from '../images/betulait.webp';
</script>

<template>
  <section id="o-nas">
    <h2 data-aos="zoom-in-up">O nas</h2>
    <div class="section-content">
      <img :src=building alt="siedziba firmy Betula IT" data-aos="zoom-in-up" />
      <p data-aos="zoom-in-up"><span id="about-logo">Betula IT</span> oferuje profesjonalne usługi informatyczne dla firm w Kwidzynie i okolicach. Doświadczony zespół ekspertów zapewnia klientom sprawną i skuteczną pomoc w rozwiązywaniu problemów, a także kompleksowe wsparcie techniczne. Odpowiadamy za prawidłowe funkcjonowanie systemów informatycznych oraz wdrażanie rozwiązań dopasowanych do potrzeb i wymagań klientów.<br /><br />
      Zapraszamy do skorzystania z naszych usług!</p>
    </div>
  </section>
</template>

<style scoped>
.section-content {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 50px;
  text-align: justify;
  line-height: 1.5;
  padding-bottom: 40px;
}

#about-logo {
  color: var(--orange);
  font-weight: 600;
}

img {
  width: 80vw;
  height: 80vw;
  max-width: 400px;
  max-height: 400px;
  box-shadow: 0px 0px 5px #30287b51;
  /* border: 1px solid #30287b4d; */
  /* border-radius: 20px; */
}

@media screen and (max-width: 1100px) {
  .section-content {
    flex-wrap: wrap;
  }
}
</style>