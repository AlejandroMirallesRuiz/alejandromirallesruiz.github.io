<script setup>
import { ref } from 'vue';

import projectInfo from '/portfolio-info/projects.json';

const ICONS = {
  "Camera": "bi-camera-video",
  "HumanProfile": "bi-file-earmark-person-fill"
}

const modals = ref([]); // Refs a los modales
const activeModal = ref(null); // Guardará el índice del modal activo

const openModal = async (index) => {
  
  activeModal.value = index;

};

const closeModal = () => {
  activeModal.value = null;
};

const projects = projectInfo["projects"]

//Swiper code
import { Navigation, Pagination, Autoplay } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/autoplay';

let modules = [Navigation, Pagination, Autoplay];

let paginationConfig = {
    type: "bullets",
    clickable: true
}
</script>

<template>
    <!-- Projects Section -->
    <section id="projects" class="projects section">

        <!-- Section Title -->
        <div class="container section-title" data-aos="fade-up">
        <h2><i class="bi bi-folder navicon"></i> Proyectos</h2>        
        </div><!-- End Section Title -->

        <div class="container">

          <div class="row gy-4">

            <div v-for="(project, index) in projects" :key="index" @click="openModal(index)" class="col-lg-4 col-md-6 project-item d-flex" data-aos="fade-up" data-aos-delay="200" id="openModal">
                <div class="icon flex-shrink-0"><i class="bi" :class="ICONS[project.icon]"></i></div>
                <div>
                    <h4 class="title">{{project.name }}</h4><h5 class="subtitle">{{ project.technologies.split(", ").slice(0, 3).join(", ") }}</h5>
                    <p class="description">{{ project.smallDescription }}</p>
                </div>
            </div>

            <section v-for="(project, index) in projects" :key="'modal-' + index" ref="modals" :class="{ 'activeModal': activeModal === index }" class="project-modal"  @click.self="closeModal">    
                <div class="container modal-content" data-aos="fade-up" data-aos-delay="100">
                  <span @click="closeModal" class="close">&times;</span>

                  <div class="row gy-4">

                    <div class="col-lg-8">
                      <div class="project-details-slider swiper init-swiper">

                        <swiper class="swiper-wrapper align-items-center"
                          :modules="modules"
                          :slides-per-view="'auto'"
                          :loop="true"
                          :speed="600"
                          navigation
                          :pagination="paginationConfig"
                          :autoplay="{ delay: 5000}"
                        >

                          <swiper-slide class="swiper-slide" v-for="slide in project.multimedia">
                            <img class="img-fluid" :src="slide" alt="">
                          </swiper-slide>

                        </swiper>
                        <div class="swiper-pagination"></div>
                      </div>
                    </div>

                    <div class="col-lg-4">
                      <div class="portfolio-info" data-aos="fade-up" data-aos-delay="200">
                        <h2>{{ project.name }}</h2>
                        <ul>
                          <li><strong>Tecnologías más destacadas</strong>: {{ project.technologies }}</li>
                          <li><strong>URL</strong>: 
                            <a v-if="project.url != ''" :href="'https://' + project.url">{{ project.url }}</a>
                            <span v-else>Contenido no disponible</span>
                          </li>
                          <li><strong>Código</strong>: 
                            <a v-if="project.url != ''" :href="project.url">Código</a>
                            <span v-else>Código no disponible</span>
                          </li>
                        </ul>
                      </div>
                      <br/>
                      <div class="portfolio-description" data-aos="fade-up" data-aos-delay="300">
                        <h2>{{ project.fullname }}</h2>
                        <p v-for="paragraph in project.wholeDescription.split('\n')">{{ paragraph }} </p>
                      </div>
                    </div>

                  </div>

                </div>
            </section>
            
            
          </div>

        </div>

    </section><!-- /projects Section -->

</template>

<style scoped>
.activeModal {
  display: block !important;
  margin-top: 0px;
}
</style>