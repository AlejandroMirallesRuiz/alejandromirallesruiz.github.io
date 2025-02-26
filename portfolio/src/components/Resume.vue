<script setup>
import resumeInfo from '/portfolio-info/resume.json';
const education = resumeInfo["education"];
const jobs = resumeInfo["workExperience"];

education.sort((a, b) => b.endDateYear - a.endDateYear);
jobs.sort((a, b) => b.endDateYear - a.endDateYear);


</script>

<template>
    <!-- Resume Section -->
    <section id="resume" class="resume section">

        <!-- Section Title -->
        <div class="container section-title" data-aos="fade-up">
        <h2><i class="bi bi-file-earmark-text navicon"></i>  Currículum Vitae</h2>
        <div class="container">

            <div class="row">

            <div class="col-lg-6" data-aos="fade-up" data-aos-delay="100">
                <h3 class="resume-title">Educación</h3>

                <div v-for="degree in education" class="resume-item">
                    <h4>{{ degree.name }}, {{ degree.title }}</h4>
                    <h5>{{degree.startDate}} - {{degree.endDate}}</h5>
                    <p><em>{{ degree.centre }}</em></p>
                    
                </div><!-- Edn Resume Item -->
            </div>

            <div class="col-lg-6" data-aos="fade-up" data-aos-delay="200">
                <h3 class="resume-title">Experiencia Profesional</h3>

                <div v-for="work in jobs" class="resume-item">
                    <h4>{{ work.position }}</h4>
                    <h5>{{ work.startDate}} - {{work.endDate}}</h5>
                    <p><em>{{ work.company }}</em></p>
                    <ul>
                        <li v-for="responsability in work.responsabilities">{{ responsability }}</li>
                    </ul>
                </div><!-- Edn Resume Item -->

            </div>

            </div>

        </div>
        </div><!-- End Section Title -->

        </section><!-- /Resume Section -->
</template>