<script setup>
import { Typed } from "@duskmoon/vue3-typed-js";

const positions = ["Web Developer", "Full-Stack Developer", "Back-End Developer", "Developer"]

const typeConfig = {
    strings: positions,
    loop: true,
    typeSpeed: 100,
    backSpeed: 50,
    backDelay: 2000
};

</script>

<template>
    <!-- Hero Section -->
    <section id="hero" class="hero section dark-background">

    <img src="/img/hero-bg.jpg" alt="" data-aos="fade-in" class="">

    <div class="container" data-aos="fade-up" data-aos-delay="100">
    <h2>Alejandro Miralles</h2>
    <Typed :options="typeConfig" >
        <p>Soy <span class="typing"></span><span class="typed-cursor typed-cursor--blink" aria-hidden="true"></span><span class="typed-cursor typed-cursor--blink" aria-hidden="true"></span></p>
    </Typed>

    </div>

    </section><!-- /Hero Section -->
</template>