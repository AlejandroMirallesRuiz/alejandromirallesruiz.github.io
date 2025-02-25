<script setup>
</script>

<template>
    <header id="header" class="header dark-background d-flex flex-column">
        <i class="header-toggle d-xl-none bi bi-list"></i>

        <div class="profile-img">
        <img src="/img/my-profile-img.jpg" alt="" class="img-fluid rounded-circle">
        </div>

        <a href="index.html" class="logo d-flex align-items-center justify-content-center">
        <!-- Uncomment the line below if you also wish to use an image logo -->
        <!-- <img src="/public/img/logo.png" alt=""> -->
        <h1 class="sitename">Alejandro Miralles</h1>
        </a>

        <div class="social-links text-center">
        <a href="https://github.com/AlejandroMirallesRuiz" class="github"><i class="bi bi-github"></i></a>
        <a href="https://www.linkedin.com/in/alejandro-miralles-ruiz/" class="linkedin"><i class="bi bi-linkedin"></i></a>
        <a href="mailto:Miralles.Ruiz.Alejandro@gmail.com?body=Hola%20Alejandro," target="_blank" class="mail"><i class="bi bi-envelope"></i></a>
        
        </div>

        <nav id="navmenu" class="navmenu">
        <ul>
            <li><a href="#hero" class="active"><i class="bi bi-house navicon"></i>Home</a></li>
            <li><a href="#about"><i class="bi bi-person navicon"></i> Sobre mí</a></li>
            <li><a href="#resume"><i class="bi bi-file-earmark-text navicon"></i> Currículum Vitae</a></li>
            <li><a href="#projects"><i class="bi bi-folder navicon"></i> Proyectos</a></li>
            <li><a href="#skills"><i class="bi bi-laptop navicon"></i> Tecnologías</a></li>
        </ul>
        </nav>

  </header>
</template>