<template>
    <section id="inicio" class="min-vh-100 d-flex align-items-center">
        <div class="container text-center">
            <div class="profile-img-container mb-4">
                <div class="profile-img-wrapper rounded-circle mx-auto">
                    <img src="@/assets/me.jpg" alt="Leandro" class="profile-img" />
                </div>
            </div>
            <h1 class="display-4 mb-4 typewriter">Olá, sou Leandro Campos</h1>
            <p class="lead mb-5">
                Navegando da curiosidade ao código, estou redesenhando minha trajetória profissional no universo tech. Apaixonado por front-end hoje, visionário full-stack amanhã. Minha missão é dominar as tecnologias que movem o mercado e construir interfaces e sistemas que não apenas funcionem, mas que transformem experiências e simplifiquem vidas.
            </p>
            <div class="button-group">
                <a href="#projetos" class="btn btn-modern me-3">Ver Projetos</a>
                <a href="#contato" class="btn btn-outline-modern me-3">Contato</a>
                <a href="/public/curriculoDev.pdf" 
                   download="Leandro_Campos_CV.pdf"
                   class="btn btn-outline-light">
                   <i class="bi bi-download me-2"></i>Currículo
                </a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "HomeSection",
};
</script>

<style scoped>
section {
    background: linear-gradient(135deg, #00bbf9 0%, #1e3a8a 100%);
    position: relative;
    overflow: hidden;
}

.geometric-shapes {
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%; 
    z-index: 1;
}

.shape {
    position: absolute;
    opacity: 0.8;
}


@keyframes float {
    0% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(5deg); }
    100% { transform: translateY(0) rotate(0deg); }
}

.container {
    position: relative;
    z-index: 2;
}

.profile-img-wrapper {
    width: 300px;
    height: 300px;
    border: 4px solid #ffffff;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.btn-modern {
    background: #ffffff;
    color: #00bbf9;
    border: none;
    padding: 12px 30px;
    border-radius: 25px;
    transition: all 0.3s ease;
}

.btn-modern:hover {
    background: #f8f9fa;
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(255, 255, 255, 0.3);
}

.btn-outline-modern {
    border: 2px solid #ffffff;
    color: #ffffff;
    padding: 12px 30px;
    border-radius: 25px;
    transition: all 0.3s ease;
}

.btn-outline-modern:hover {
    background: #ffffff;
    color: #00bbf9;
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(255, 255, 255, 0.3);
}

.lead {
    color: #ffffff;
    max-width: 700px;
    margin: 0 auto;
    line-height: 1.8;
}

h1 {
    color: #ffffff;
    font-weight: 600;
}

/* responsividade */
@media (max-width: 768px) {
    .geometric-shapes {
        width: 100%;
        opacity: 0.3;
    }
    
    .profile-img-wrapper {
        width: 200px;
        height: 200px;
    }
    
    .button-group {
        flex-direction: column;
        align-items: center;
    }
    
    .button-group .btn {
        width: 200px;
        margin: 5px 0;
    }

    .btn-outline-dark {
        width: 200px;
        margin: 5px 0;
    }
}

.profile-img-container {
    width: 400px;
    height: 400px;
    margin: 0 auto;
}

.profile-img-wrapper {
    width: 100%;
    height: 100%;
    overflow: hidden;
    position: relative;
}

.profile-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    top: 0;
    left: 0;
}

.button-group {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 2rem;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.typewriter {
    overflow: hidden;
    border-right: .15em solid #ffffff;
    white-space: nowrap;
    margin: 0 auto;
    animation: 
        typing 4.5s steps(40, end),
        blink-caret .75s step-end infinite;
}

@keyframes typing {
    from { width: 0 }
    to { width: 50% }
}

@keyframes blink-caret {
    from, to { border-color: transparent }
    40% { border-color: #ffffff }
}

.btn-outline-dark {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 12px 30px;
    border-radius: 25px;
    transition: all 0.3s ease;
    gap: 0.5rem;
}

.btn-outline-dark:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.btn-outline-dark i {
    font-size: 1rem;
    line-height: 1;
}
</style>