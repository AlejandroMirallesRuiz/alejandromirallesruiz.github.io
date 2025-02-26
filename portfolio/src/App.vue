<script setup>
  import FooterComponent from './components/Footer.vue';
  import HeaderComponent from './components/Header.vue';

  import HeroSection from './components/Hero.vue';
  import AboutSection from './components/About.vue';
  import ResumeSection from './components/Resume.vue';
  import SkillSection from './components/Skills.vue';

  import ProjectSection from './components/Project.vue';
</script>

<template>

  <HeaderComponent />

  <main class="main">

    <HeroSection />

    <AboutSection />

    <ResumeSection />

    <ProjectSection />

    <SkillSection />

    
  </main>

  <FooterComponent />

  <!-- Scroll Top -->
  <a href="#" id="scroll-top" class="scroll-top d-flex align-items-center justify-content-center"><i class="bi bi-arrow-up-short"></i></a>

  <!-- Preloader -->
  <div id="preloader"></div>

</template>