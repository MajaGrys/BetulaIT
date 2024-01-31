<script setup>
import building from '../images/betulait.webp';
import ziarnpol from '../images/ziarnpol.webp';
import sebteam from '../images/seb-team.webp';
</script>

<template>
  <section id="o-nas">
    <h2 data-aos="zoom-in-up">O nas</h2>
    <div class="section-content">
      <img :src=building alt="siedziba firmy Betula IT" data-aos="zoom-in-up" class="building" />
      <div>
        <p data-aos="zoom-in-up"><span id="about-logo">Betula IT</span> oferuje profesjonalne usługi informatyczne dla firm w Kwidzynie i okolicach. Doświadczony zespół ekspertów zapewnia klientom sprawną i skuteczną pomoc w rozwiązywaniu problemów, a także kompleksowe wsparcie techniczne. Odpowiadamy za prawidłowe funkcjonowanie systemów informatycznych oraz wdrażanie rozwiązań dopasowanych do potrzeb i wymagań klientów.</p><br />
        <p data-aos="zoom-in-up">Zaufali nam:<br />
          <div class="logos">
            <a href="http://www.ziarnpol.pl/"><img :src=ziarnpol alt="Ziarnpol" /></a>
            <a href="https://seb-team.pl/"><img :src=sebteam alt="Seb-team" /></a>
          </div>
        </p>
      </div>
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

.building {
  width: 80vw;
  height: 80vw;
  max-width: 400px;
  max-height: 400px;
  box-shadow: 0px 0px 5px #30287b51;
}

.logos {
  display: flex;
  gap: 20px;
  align-items: center;
  
  img {
    max-width: 200px;
    max-height: 100px;
    transition: 0.5s;
    
    &:hover {
      transform: scale(1.1);
      transition: 0.5s;
    }
  }
}

@media screen and (max-width: 1100px) {
  .section-content {
    flex-wrap: wrap;
  }
}
</style>