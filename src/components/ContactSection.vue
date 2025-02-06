<template>
    <section id="contato" class="py-5 bg-white">
        <div class="container">
            <h2 class="text-center mb-5">Contato</h2>
            <div class="row justify-content-center">
                <div class="col-md-8 text-center">
                    <div class="social-links mb-4">
                        <a href="https://www.linkedin.com/in/leandro-campos-dev/" 
                           target="_blank" 
                           class="social-link me-4">
                            <i class="bi bi-linkedin"></i>
                            <span>LinkedIn</span>
                        </a>
                        <a href="https://github.com/LeandroCamposDEV" 
                           target="_blank" 
                           class="social-link me-4">
                            <i class="bi bi-github"></i>
                            <span>GitHub</span>
                        </a>
                        <a href="mailto:leandro.f.ti@outlook.com" 
                           class="social-link">
                            <i class="bi bi-envelope-fill"></i>
                            <span>E-mail</span>
                        </a>
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
.social-links {
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.social-link {
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #333;
    text-decoration: none;
    transition: transform 0.3s ease, color 0.3s ease;
    padding: 1rem;
}

.social-link:hover {
    transform: translateY(-5px);
    color: var(--primary-color);
}

.social-link i {
    font-size: 2rem;
    margin-bottom: 0.5rem;
}

.social-link span {
    font-size: 1rem;
}

/* Cores específicas para cada rede no hover */
.social-link:hover i.bi-linkedin {
    color: #0077b5;
}

.social-link:hover i.bi-github {
    color: #333;
}

.social-link:hover i.bi-envelope-fill {
    color: #ea4335;
}

/* Responsividade */
@media (max-width: 768px) {
    .social-links {
        flex-direction: column;
        gap: 1rem;
    }

    .social-link {
        flex-direction: row;
        justify-content: center;
        gap: 1rem;
    }

    .social-link i {
        margin-bottom: 0;
    }
}
</style>