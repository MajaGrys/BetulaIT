<script setup>
import email from '../images/icon-mail.svg';
import phone from '../images/icon-phone.svg';
import location from '../images/icon-map-pin.svg';
</script>

<template>
    <section id="kontakt">
        <h2 data-aos="zoom-in-up">Kontakt</h2>
        <div class="section-content">
            <iframe
                loading="lazy"
                src="https://www.google.com/maps/embed/v1/place?q=Fryderyka+Chopina+24,+Kwidzyn,+Polska&key=AIzaSyBFw0Qbyq9zTFTd-tUY6dZWTgaQzuU17R8"
                title="Betula IT"
                data-aos="zoom-in-up">
            </iframe>

            <div class="contact-info" data-aos="zoom-in-up">
                <div><img :src=location alt="" />
                    Fryderyka Chopina 24, 82-500 Kwidzyn<br />
                    <div class="godziny-otwarcia">
                        <div>Godziny otwarcia:</div>
                        <div>Pon-Pt: 8:00-16:00<br />
                             Sob-Nd: nieczynne</div>
                    </div>
                </div>
                <div><img :src=phone alt="" /> +48 501 403 018</div>
                <a href="mailto:lukaszbrzoza@gmail.com"><img :src=email alt="" /> lukaszbrzoza@gmail.com</a>
            </div>
        </div>
    </section>
</template>

<style scoped>
.section-content {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px 50px;
    line-height: 2.5;
    font-size: 1.2rem;
    padding-bottom: 80px;
}

iframe {
    border: none;
    border-radius: var(--radius);
    width: 90vw;
    height: 50vh;
    max-width: 500px;
    max-height: 400px;
}

img {
    filter: invert(1);
    height: 20px;
    transform: translateY(3px);
}

.godziny-otwarcia {
    display: grid;
    grid-template-columns: 1fr;
}

@media screen and (min-width: 512px) {
    .godziny-otwarcia {
        grid-template-columns: 1fr 1fr;
    }
}

a {
    color: white;
    text-decoration: none;
    transition: var(--transition);
}
</style>