<script setup>
import office from '../images/student-849825_1920.jpg';
import building from '../images/street-5030692_1280.jpg';
</script>

<template>
  <section id="o-nas">
    <h2>O nas</h2>
    <div class="section-content">
      <img :src=building />
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque illo quia mollitia officia laudantium aliquam fugiat illum fuga eligendi quam, consectetur magni quaerat tempora quibusdam harum? Molestiae inventore ut error reiciendis, aspernatur commodi exercitationem! Vero, delectus a porro distinctio non dolorem dolorum quam id fugiat, blanditiis officia magni explicabo eius quaerat aut provident natus exercitationem? <br /><br />
      Ut fuga soluta sunt quis sequi, iure distinctio, dignissimos exercitationem, deleniti fugiat quas! Non cum temporibus blanditiis officia deleniti! Qui ipsum suscipit, quisquam natus accusantium aliquam, accusamus earum dignissimos modi nostrum et illum soluta maxime commodi rem odio voluptatibus optio adipisci quis. Deleniti, iure illo!<br /><br />
      Quaerat maxime, atque magni eum soluta temporibus id nobis est, labore dolorum vel voluptatum sunt ad esse!</p>
    </div>
    
    <!-- <div class="section-content">
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum maxime possimus laudantium cupiditate assumenda consectetur ipsum numquam laborum deserunt officiis ipsam, alias magnam voluptatibus! Cupiditate, magni nulla obcaecati reprehenderit ut qui quia rerum quasi, autem modi architecto possimus porro enim error, necessitatibus exercitationem at explicabo eos mollitia aliquid alias labore ab impedit esse.<br /><br />
      Quibusdam perferendis nobis dolor, beatae odit provident impedit a quia neque. Iusto, quibusdam. Quasi, iure doloribus debitis minus sunt, praesentium esse aliquid magni, perferendis laboriosam rem? Impedit non officiis dicta debitis nemo fugit odit saepe!</p>
      <img :src=office />
    </div> -->
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

img {
  width: 80vw;
  height: 80vw;
  max-width: 400px;
  max-height: 400px;
  /* box-shadow: 0px 0px 5px var(--black); */
  /* border-radius: 20px; */
}

@media screen and (max-width: 1100px) {
  .section-content {
    flex-wrap: wrap;
  }
}
</style>