<script setup>
import building from '../images/betulait.webp';
import ziarnpol from '../images/ziarnpol.webp';
import sebteam from '../images/seb-team.webp';
import kalinabhp from '../images/kalina-bhp.png';
import sp2 from '../images/sp2.png';
</script>

<template>
  <section id="o-nas">
    <h2 data-aos="zoom-in-up">O nas</h2>
    <div class="section-content">
      <img :src=building alt="siedziba firmy Betula IT" data-aos="zoom-in-up" class="building" />
      <div>
        <p data-aos="zoom-in-up">Betula IT wykonuje profesjonalne usługi informatyczne dla firm w Kwidzynie i okolicach zarówno na miejscu, jak i zdalnie. Doświadczony zespół ekspertów zapewnia klientom sprawną i skuteczną pomoc w rozwiązywaniu problemów, a także kompleksowe wsparcie techniczne. Odpowiadamy za prawidłowe funkcjonowanie systemów informatycznych oraz wdrażanie rozwiązań dopasowanych do potrzeb i wymagań klientów.</p><br />
        <p data-aos="zoom-in-up">Instytucje, które nam zaufały<br />
          <div class="logos">
            <a href="http://www.ziarnpol.pl/"><img :src=ziarnpol alt="Ziarnpol" /></a>
            <a href="https://seb-team.pl/"><img :src=sebteam alt="Seb-team" /></a>
            <a href="https://bhp-kwidzyn.pl/"><img :src=kalinabhp alt="Kalina Usługi BHP" /></a>
            <a href="https://www.sp2.kwidzyn.pl/"><img :src=sp2 alt="Szkoła Podstawowa nr 2 w Kwidzynie" /></a>
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
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 20px;
  
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