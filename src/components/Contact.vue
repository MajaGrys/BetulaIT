<script setup>
import email from '../images/mail.svg';
import phone from '../images/phone.svg';
import location from '../images/map-pin.svg';
</script>

<template>
    <section id="kontakt">
        <h2>Kontakt</h2>
        <div class="section-content">
            <iframe
                loading="lazy"
                src="https://www.google.com/maps/embed/v1/place?q=Fryderyka+Chopina+24,+Kwidzyn,+Polska&key=AIzaSyBFw0Qbyq9zTFTd-tUY6dZWTgaQzuU17R8"
                title="Betula IT">
            </iframe>

            <div class="contact-info">
                <div><img :src=location />
                    Fryderyka Chopina 24, 82-500 Kwidzyn<br />
                    Godziny otwarcia:<br />
                    Pon-Pt: 8:00-16:00<br />
                    Sob-Nd: nieczynne
                </div>
                <div><img :src=phone /> +48 501 403 018</div>
                <a href="mailto:lukaszbrzoza@gmail.com"><img :src=email /> lukaszbrzoza@gmail.com</a>
            </div>
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: var(--purple);
    color: white;
}

.section-content {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px 50px;
    line-height: 2.5;
    padding-bottom: 80px;
}

iframe {
    border: none;
    border-radius: 10px;
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

a {
    color: white;
    text-decoration: none;
    transition: 0.5s;
}
</style>