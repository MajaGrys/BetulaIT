<script setup>
import building from '../images/betula.webp';
</script>

<template>
  <section id="o-nas">
    <h2 data-aos="zoom-in-up">O nas</h2>
    <div class="section-content">
      <img :src=building alt="siedziba firmy BetulaIT" data-aos="zoom-in-up" />
      <p data-aos="zoom-in-up"><span id="logo">BetulaIT</span> lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque illo quia mollitia officia laudantium aliquam fugiat illum fuga eligendi quam, consectetur magni quaerat tempora quibusdam harum? Molestiae inventore ut error reiciendis, aspernatur commodi exercitationem! Vero, delectus a porro distinctio non dolorem dolorum quam id fugiat, blanditiis officia magni explicabo eius quaerat aut provident natus exercitationem?<br /><br />
      Ut fuga soluta sunt quis sequi, iure distinctio, dignissimos exercitationem, deleniti fugiat quas! Non cum temporibus blanditiis officia deleniti! Qui ipsum suscipit, quisquam natus accusantium aliquam, accusamus earum dignissimos modi nostrum et illum soluta maxime commodi rem odio voluptatibus optio adipisci quis. Deleniti, iure illo!<br /><br />
      Quaerat maxime, atque magni eum soluta temporibus id nobis est, labore dolorum vel voluptatum sunt ad esse!</p>
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

#logo {
  font-size: 1.2rem;
  color: var(--orange);
  font-weight: 600;
}

img {
  width: 80vw;
  height: 80vw;
  max-width: 400px;
  max-height: 400px;
  /* box-shadow: 0px 0px 5px var(--black); */
  /* border: 1px solid var(--purple); */
  /* border-radius: 20px; */
}

@media screen and (max-width: 1100px) {
  .section-content {
    flex-wrap: wrap;
  }
}
</style>