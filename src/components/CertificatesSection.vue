<template>
    <section id="certificados" class="min-vh-100 py-5">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Certificados e Cursos</h2>
            <div class="row g-4">
                <div v-for="cert in certificates" :key="cert.title" class="col-md-6 col-lg-4">
                    <div class="certificate-card h-100">
                        <a :href="cert.link" 
                           :target="isExternalLink(cert.link) ? '_blank' : ''"
                           :download="!isExternalLink(cert.link)"
                           class="text-decoration-none">
                            <div class="card-image-wrapper">
                                <img :src="cert.image" class="card-img-top" :alt="cert.title">
                            </div>
                            <div class="card-body">
                                <h5 class="card-title">{{ cert.title }}</h5>
                                <p class="card-text">{{ cert.institution }}</p>
                                <div class="view-certificate">
                                    <span class="certificate-link">
                                        <i class="bi" :class="isExternalLink(cert.link) ? 'bi-arrow-up-right' : 'bi-download'"></i>
                                        {{ isExternalLink(cert.link) ? 'Ver Certificado' : 'Download Certificado' }}
                                    </span>
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
section {
    background: linear-gradient(135deg, #00bbf9 0%, #1e3a8a 100%);
    padding-top: 80px;
    position: relative;
    overflow: hidden;
}

h2 {
    color: #ffffff;
    font-weight: 700;
    margin-bottom: 3rem;
}

.certificate-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
    transition: all 0.3s ease;
    border: none;
}

.certificate-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
}

.card-image-wrapper {
    position: relative;
    overflow: hidden;
    height: 200px;
}

.card-img-top {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.certificate-card:hover .card-img-top {
    transform: scale(1.05);
}

.card-body {
    padding: 1.5rem;
}

.card-title {
    color: #1e3a8a;
    font-size: 1.1rem;
    font-weight: 600;
    line-height: 1.4;
    margin-bottom: 0.75rem;
}

.card-text {
    color: #4a5568;
    font-size: 0.9rem;
    margin-bottom: 1rem;
}

.view-certificate {
    margin-top: auto;
}

.certificate-link {
    background: linear-gradient(135deg, #00bbf9 0%, #1e3a8a 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 0.9rem;
    font-weight: 500;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    transition: all 0.3s ease;
}

.certificate-link i {
    font-size: 1.1rem;
    background: linear-gradient(135deg, #00bbf9 0%, #1e3a8a 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

@media (max-width: 768px) {
    section {
        padding-top: 60px;
    }
    
    .card-image-wrapper {
        height: 180px;
    }
    
    .card-body {
        padding: 1.25rem;
    }
}

@media (max-width: 375px) {
    .card-body {
        padding: 1rem;
    }
    
    .card-title {
        font-size: 1rem;
    }
    
    .card-text {
        font-size: 0.85rem;
    }
    
    .certificate-link {
        font-size: 0.85rem;
    }
}
</style>