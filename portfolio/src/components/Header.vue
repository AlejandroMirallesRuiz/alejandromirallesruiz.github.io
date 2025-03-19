<script setup>
import { ref} from 'vue'
// Nav menu
const menuOptions = [
    {
     name: "Home",
     icon: "bi-house",
     id: "hero",   
    },
    {
     name: "Sobre mí",
     icon: "bi-person",
     id: "about",   
    },
    {
     name: "Currículum Vitae",
     icon: "bi-file-earmark-text",
     id: "resume",   
    },
    {
     name: "Proyectos",
     icon: "bi-folder",
     id: "projects",   
    },
    {
     name: "Tecnologías",
     icon: "bi-laptop",
     id: "skills",   
    },
]

// Menu icon
const isHeaderVisible = ref(false);

const toggleHeader = () => {
  isHeaderVisible.value = !isHeaderVisible.value;
};

const hideNav = () => {
  if (isHeaderVisible.value) {
    toggleHeader();
  }
};

function closeNav(){
    isHeaderVisible.value = false
}
</script>

<template>
    <header id="header" class="header dark-background d-flex flex-column" :class="isHeaderVisible ? 'header-show' : ''"  @click.self="closeNav">
        <i @click="toggleHeader" class="header-toggle d-xl-none bi" :class="isHeaderVisible ? 'bi-x' : 'bi-list'"></i>

        <div class="profile-img">
        <img src="/img/Foto_CV2.jpeg" alt="" class="img-fluid rounded-circle">
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
            <li v-for="(option, index) in menuOptions">
                <a :href="`#${option.id}`" class="active" @click="hideNav">
                    <i class="bi navicon" :class="option.icon, { active: index === 0 }"></i>{{option.name}}
                </a>
            </li>
        </ul>
        </nav>

  </header>
</template>