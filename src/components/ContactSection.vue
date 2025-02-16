<template>
    <section id="contato" class="min-vh-100 py-5">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Contato</h2>
            <div class="row justify-content-center">
                <div class="col-md-8">
                    <div class="contact-card">
                        <h3 class="text-center mb-4">Vamos Conversar?</h3>
                        <p class="text-center mb-5">
                            Estou sempre aberto a novas oportunidades e colaborações.
                        </p>
                        <div class="social-links">
                            <a href="https://www.linkedin.com/in/leandro-campos-dev/" 
                               target="_blank" 
                               class="social-link">
                                <div class="icon-wrapper">
                                    <i class="bi bi-linkedin"></i>
                                </div>
                                <span>LinkedIn</span>
                            </a>
                            <a href="https://github.com/LeandroCamposDEV" 
                               target="_blank" 
                               class="social-link">
                                <div class="icon-wrapper">
                                    <i class="bi bi-github"></i>
                                </div>
                                <span>GitHub</span>
                            </a>
                            <a href="mailto:leandro.f.ti@outlook.com" 
                               class="social-link">
                                <div class="icon-wrapper">
                                    <i class="bi bi-envelope-fill"></i>
                                </div>
                                <span>E-mail</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ContactSection'
}
</script>

<style scoped>
section {
    background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
    padding-top: 80px;
}

h2 {
    color: #2d2d2d;
    font-weight: 700;
    margin-bottom: 3rem;
}

.contact-card {
    background: white;
    border-radius: 15px;
    padding: 3rem 2rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
}

.contact-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
}

h3 {
    color: #2d2d2d;
    font-weight: 600;
    font-size: 1.75rem;
}

p {
    color: #666;
    font-size: 1.1rem;
}

.social-links {
    display: flex;
    justify-content: center;
    gap: 2.5rem;
}

.social-link {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-decoration: none;
    transition: all 0.3s ease;
}

.icon-wrapper {
    width: 70px;
    height: 70px;
    background: rgba(155, 93, 229, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1rem;
    transition: all 0.3s ease;
}

.social-link i {
    font-size: 2rem;
    transition: all 0.3s ease;
}

.social-link span {
    color: #4a4a4a;
    font-size: 1rem;
    font-weight: 500;
    transition: all 0.3s ease;
}

/* Hover states */
.social-link:hover .icon-wrapper {
    transform: translateY(-5px);
}

.social-link:hover i.bi-linkedin {
    color: #0077b5;
}

.social-link:hover i.bi-github {
    color: #333;
}

.social-link:hover i.bi-envelope-fill {
    color: #ea4335;
}

@media (max-width: 768px) {
    section {
        padding-top: 60px;
    }

    .contact-card {
        padding: 2rem 1rem;
    }

    .social-links {
        flex-direction: column;
        gap: 2rem;
    }

    .social-link {
        flex-direction: row;
        gap: 1rem;
    }

    .icon-wrapper {
        width: 60px;
        height: 60px;
        margin-bottom: 0;
    }
}
</style>