<script setup>
import skillsInfo from '/portfolio-info/skills.json';
const skills = skillsInfo['skills'];

// import Swiper core and required modules
import { Navigation, Pagination, Autoplay } from 'swiper/modules';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/autoplay';

let modules = [Navigation, Pagination, Autoplay];
let breakpointsConfig = {
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
let paginationConfig = {
    type: "bullets",
    clickable: true
}

/*
// Original config
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
*/
</script>

<template>
    <!-- Skills Section -->
    <section id="skills" class="section light-background testimonials">

        <!-- Section Title -->
        <div class="container section-title" data-aos="fade-up">
        <h2><i class="bi bi-laptop navicon"></i> Tecnologías</h2>

        <div class="swiper-skills swiper init-swiper">
            <swiper
                :modules="modules"
                :slides-per-view="'auto'"
                :loop="true"
                :effect="'slide'"
                :cssMode="false"
                :speed="3000"
                navigation
                :pagination="paginationConfig"
                :autoplay="{ delay: 1000, disableOnInteraction: false}"
                :breakpoints="breakpointsConfig"
            >
              <swiper-slide v-for="skill in skills" class="swiper-slide">
                <div class="testimonial-item">
                    <img :src="skill.image" class="testimonial-img" alt="">
                  <h3>{{ skill.name }}</h3>
                </div>
              </swiper-slide>


            </swiper>
        </div>
        </div><!-- End Section Title -->



    </section><!-- /Skills Section -->
</template>