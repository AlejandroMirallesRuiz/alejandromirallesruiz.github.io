<script setup>
import { onMounted } from 'vue';

import Swiper from 'swiper';
import 'swiper/css';


onMounted(() => {
    new Swiper('.swiper-skills', {
      loop: true,
      effect: "slide",
      cssMode: false,
      speed: 3000,
      autoplay: {
        delay: 1000,
        disableOnInteraction: false
      },
      slidesPerView: "auto",
      pagination: {
        el: ".swiper-pagination",
        type: "bullets",
        clickable: true
      },
      breakpoints: {
        320: {
          slidesPerView: 1,
          spaceBetween: 40
        },
        650: {
          slidesPerView: 2,
          spaceBetween: 10
        },
        800: {
          slidesPerView: 3,
          spaceBetween: 10
        },
        1200: {
          slidesPerView: 4,
          spaceBetween: 10
        }
      }
    });
});
</script>

<template>
    <!-- Skills Section -->
    <section id="skills" class="section light-background testimonials">

        <!-- Section Title -->
        <div class="container section-title" data-aos="fade-up">
        <h2><i class="bi bi-laptop navicon"></i> Tecnologías</h2>

        <div class="swiper-skills- swiper init-swiper">
            
            <div class="swiper-wrapper">
            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/MySQL.png" class="testimonial-img" alt="">
                <h3>MySQL</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/MongoDb.png" class="testimonial-img" alt="">
                <h3>MongoDB</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/redis.png" class="testimonial-img" alt="">
                <h3>Redis</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/docker.png" class="testimonial-img" alt="">
                <h3>Docker</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/bootstrap.png" class="testimonial-img" alt="">
                <h3>Boostrap</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/nodejs.png" class="testimonial-img" alt="">
                <h3>NodeJS</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/Symphony.png" class="testimonial-img" alt="">
                <h3>Symphony</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/yii.png" class="testimonial-img" alt="">
                <h3>Yii</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/vuejs.png" class="testimonial-img" alt="">
                <h3>Vue.js</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/Jquery.png" class="testimonial-img" alt="">
                <h3>Jquery</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/python.png" class="testimonial-img" alt="">
                <h3>Python</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/php.png" class="testimonial-img" alt="">
                <h3>PHP</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/Javascript.png" class="testimonial-img" alt="">
                <h3>Javascript</h3>
                </div>
            </div><!-- End testimonial item -->

            <div class="swiper-slide">
                <div class="testimonial-item">
                <img src="/img/technologies/java.png" class="testimonial-img" alt="">
                <h3>Java</h3>
                </div>
            </div><!-- End testimonial item -->

            </div>
            <div class="swiper-pagination"></div>
        </div>
        </div><!-- End Section Title -->



        </section><!-- /Skills Section -->
</template>