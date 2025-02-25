<script setup>
import { onMounted } from 'vue';

import Swiper from 'swiper';
import 'swiper/css';


onMounted(() => {
    new Swiper('.project-details-slider', {
      loop: true,
      speed: 600,
      autoplay: {
        delay: 5000
      },
      slidesPerView: "auto",
      pagination: {
        el: ".swiper-pagination",
        type: "bullets",
        clickable: true
      }
    });
})

</script>

<template>
    <!-- Modal Section-->
    <section id="project-modal" class="project-modal">    
      <div class="container modal-content" data-aos="fade-up" data-aos-delay="100">
        <span class="close">&times;</span>

        <div class="row gy-4">

          <div class="col-lg-8">
            <div class="project-details-slider swiper init-swiper">

              <div class="swiper-wrapper align-items-center">

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/app-1.jpg" alt="">
                </div>

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/product-1.jpg" alt="">
                </div>

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/branding-1.jpg" alt="">
                </div>

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/books-1.jpg" alt="">
                </div>

              </div>
              <div class="swiper-pagination"></div>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="portfolio-info" data-aos="fade-up" data-aos-delay="200">
              <h2>Portfolio</h2>
              <ul>
                <li><strong>Tecnologías más destacadas</strong>: Vuejs, ESLint, Prettier, Bootstrap, Github pages</li>
                <li><strong>URL</strong>: <a href="#">www.example.com</a></li>
                <li><strong>Código</strong>: <a href="#">www.example.com</a></li>
              </ul>
            </div>
            <br/>
            <div class="portfolio-description" data-aos="fade-up" data-aos-delay="300">
              <h2>Portfolio de mi carrera profesional</h2>
              <p>
                Su objetivo es servir como una carta de presentación digital, permitiendo a los visitantes conocer más sobre mi trabajo y ponerse en contacto conmigo. 
              </p>
              <p>
                El uso de Bootstrap garantiza una experiencia responsiva y una navegación fluida en dispositivos móviles. Por otra parte, Vue.js facilita el mantenimiento y la actualización del sitio, optimizando su rendimiento y escalabilidad.
              </p>
            </div>
          </div>

        </div>

      </div>
    </section>

    <section id="project-modal-invisicam" class="project-modal">    
      <div class="container modal-content" data-aos="fade-up" data-aos-delay="100">
        <span id="closeButton-Invisicam" class="close">&times;</span>

        <div class="row gy-4 project-info">

          <div class="col-lg-8">
            <div class="project-details-slider swiper init-swiper">

              <div class="swiper-wrapper align-items-center">

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/app-1.jpg" alt="">
                </div>

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/product-1.jpg" alt="">
                </div>

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/branding-1.jpg" alt="">
                </div>

                <div class="swiper-slide">
                  <img class="img-fluid" src="/img/portfolio/books-1.jpg" alt="">
                </div>

              </div>
              <div class="swiper-pagination"></div>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="portfolio-info" data-aos="fade-up" data-aos-delay="200">
              <h2>Invisicam</h2>
              <ul>
                <li><strong>Tecnologías más destacadas</strong>: Nodejs, Python, Cloudflare, Jquery, Bootstrap</li>
                <li><strong>URL</strong>: No disponible</li>
                <li><strong>Código</strong>: No disponible</li>
              </ul>
            </div>
            <br/>
            <div class="portfolio-description" data-aos="fade-up" data-aos-delay="300">
              <h2>Sistema de Monitoreo con Raspberry Pi</h2>
              <p>
                Cada Raspberry cuenta con su propia página web, donde se pueden visualizar las imágenes capturadas y almacenar registros. Además, se ha desarrollado un servidor central que monitorea el estado de cada dispositivo, permitiendo verificar qué Raspberries están activas o inactivas en cualquier momento.
              </p>
              <p>
                Las Raspberries están escritas en Python, usando la librería Picamera2. Posteriormente con Cloudflare se crea un túnel para conectarse a la cámara de forma segura. <br/>
                El servidor fue escrito en Nodejs, siguiendo una arquitectura MVC. Este debe escuchar cuando se encienden las Raspberries y hacerles una llamada periodicamente para comprobar si siguen vivas.
              </p>
            </div>
          </div>

        </div>

      </div>
    </section>

</template>