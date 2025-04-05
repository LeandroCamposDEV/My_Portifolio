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
    <footer class="py-5">
      <div class="container">
        <div class="footer-content">
          <p class="copyright">
            © {{ new Date().getFullYear() }} Leandro Campos | Front-end Developer
          </p>
          <p class="made-with">
            Desenvolvido com <i class="bi bi-heart-fill text-gradient"></i> Vue.js
          </p>
        </div>
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
  background: linear-gradient(135deg, #00bbf9 0%, #1e3a8a 100%);
  padding: 2rem 0;
  position: relative;
}

.footer-content {
  text-align: center;
}

copyright {
  color: #ffffff;
  font-weight: 500;
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.made-with {
  color: rgba(255, 255, 255, 0.8);
  font-size: 0.9rem;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
}

.text-muted {
  font-size: 0.875rem;
}

.text-gradient {
  background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.1); }
}

@media (max-width: 768px) {
  footer {
    padding: 1.5rem 0;
  }
  
  .copyright {
    font-size: 0.9rem;
  }
  
  .made-with {
    font-size: 0.8rem;
  }
}

@media (max-width: 375px) {
  footer {
    padding: 1rem 0;
  }
  
  .copyright {
    font-size: 0.8rem;
  }
  
  .made-with {
    font-size: 0.75rem;
  }
}

/* Estilos globais adicionais aqui */
</style>