<template>
  <div>
    <header-section />
    <main>
      <home-section />
      <about-section />
      <projects-section />
      <skills-section />
      <certificates-section />
      <education-section />
      <objectives-section />
      <contact-section />
    </main>
    <footer class="py-4 bg-light text-center">
      <div class="container">
        <p class="mb-1">
          © {{ new Date().getFullYear() }} Leandro Campos | Front-end Developer
        </p>
        <p class="text-muted small">
          Desenvolvido com Vue.js
        </p>
      </div>
    </footer>
  </div>
 </template>
 
 <script>
 import HeaderSection from './components/HeaderSection.vue'
 import HomeSection from './components/HomeSection.vue'
 import AboutSection from './components/AboutSection.vue'
 import ProjectsSection from './components/ProjectsSection.vue'
 import SkillsSection from './components/SkillsSection.vue'
 import CertificatesSection from './components/CertificatesSection.vue'
 import EducationSection from './components/EducationSection.vue'
 import ObjectivesSection from './components/ObjectivesSection.vue'
 import ContactSection from './components/ContactSection.vue'
 
 export default {
  name: 'App',
  components: {
    HeaderSection,
    HomeSection,
    AboutSection,
    ProjectsSection,
    SkillsSection,
    CertificatesSection,
    EducationSection,
    ObjectivesSection,
    ContactSection
  }
 }
 </script>
 
 <style>
 :root {
  --primary-color: #007bff;
  --secondary-color: #6c757d;
  --background-light: #f8f9fa;
 }
 
 html {
  scroll-behavior: smooth;
 }
 
 section {
  padding-top: 80px;
 }
 
 footer {
  border-top: 1px solid rgba(0,0,0,0.1);
 }
 
 .text-muted {
  font-size: 0.875rem;
 }
 
 /* Estilos globais adicionais aqui */
 </style>