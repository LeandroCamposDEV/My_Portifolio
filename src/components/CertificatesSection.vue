<template>
    <section id="certificados" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-5">Certificados e Cursos</h2>
            <div class="row g-4">
                <div v-for="cert in certificates" :key="cert.title" class="col-md-6 col-lg-4">
                    <div class="card h-100 shadow-sm">
                        <a :href="cert.link" 
                           :target="isExternalLink(cert.link) ? '_blank' : ''"
                           :download="!isExternalLink(cert.link)"
                           class="text-decoration-none">
                            <img :src="cert.image" class="card-img-top" :alt="cert.title">
                            <div class="card-body">
                                <h5 class="card-title">{{ cert.title }}</h5>
                                <p class="card-text text-muted">{{ cert.institution }}</p>
                                <div class="mt-2">
                                    <small class="text-primary">
                                        <i class="bi" :class="isExternalLink(cert.link) ? 'bi-arrow-up-right' : 'bi-download'"></i>
                                        {{ isExternalLink(cert.link) ? 'Ver Certificado' : 'Download Certificado' }}
                                    </small>
                                </div>
                            </div> 
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'CertificatesSection',
    data() {
        return {
            certificates: [
                {
                    title: 'CS50x: Introduction to Computer Science',
                    institution: 'Harvard University',
                    image: '/certificates/CS5023.png',
                    link: 'https://certificates.cs50.io/e1a4c2ec-e612-4191-9cbb-cadd07732c03.pdf?size=letter'
                },
                {
                    title: 'CS50x: Verified Certificate EDX',
                    institution: 'EDX',
                    image: '/certificates/EDX.png',
                    link: 'https://courses.edx.org/certificates/547d758095fd40e9a4239b195b86a6c6'
                },
                {
                    title: 'Trilha Digital | Coders 24 | Front End',
                    institution: 'Ada Tech',
                    image: '/certificates/ADA.png',
                    link: 'https://ada.tech/certificado?code=bf222ee8-7e11-a8a7-717a-556de516323e'
                },
                {
                    title: 'DIO Campus Expert',
                    institution: 'DIO',
                    image: '/certificates/card_dio.png',
                    link: '/certificates/pdfs/campus10.pdf'
                },
                {
                    title: 'Bootcamp Microsoft Certification Challenge #1 - AI 102',
                    institution: 'DIO/Microsoft',
                    image: '/certificates/ai-102.png',
                    link: '/certificates/pdfs/AI-102.pdf'
                },
                {
                    title: 'Fundamentos de IA para Devs',
                    institution: 'DIO/Santander',
                    image: '/certificates/santander.png',
                    link: '/certificates/pdfs/IAparaDevs.pdf'
                },
                {
                    title: 'Inteligência Artificial e Computacional',
                    institution: 'FIAP Nano Courses',
                    image: '/certificates/fiap.png',
                    link: 'https://on.fiap.com.br/pluginfile.php/1/local_nanocourses/certificado_nanocourse/89224/63d5d573159750028f8743059223cbb2/certificado.png'
                },
                {
                    title: 'Soluções Tecnológicas Emergentes',
                    institution: 'FIAP Nano Courses',
                    image: '/certificates/fiap.png',
                    link: 'https://on.fiap.com.br/pluginfile.php/1/local_nanocourses/certificado_nanocourse/101068/b1e7e33f4a7c9a62ef868196ea84bd4f/certificado.png'
                }
            ]
        }
    },
    methods: {
        isExternalLink(link) {
            return link.startsWith('http://') || link.startsWith('https://')
        }
    }
}
</script>

<style scoped>
.card {
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
}

.card-img-top {
    height: 200px;
    object-fit: cover;
}

.card-title {
    color: #333;
    font-size: 1.1rem;
    line-height: 1.4;
    margin-bottom: 0.5rem;
}

.text-primary small {
    transition: opacity 0.3s ease;
}

.card:hover .text-primary small {
    opacity: 0.8;
}
</style>