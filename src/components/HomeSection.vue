<template>
    <section id="inicio" class="min-vh-100 d-flex align-items-center bg-light">
        <div class="container text-center">
            <div class="profile-img-container mb-4">
                <div class="profile-img-wrapper rounded-circle mx-auto">
                    <img src="@/assets/me.jpg" alt="Leandro" class="profile-img" />
                </div>
            </div>
            <h1 class="display-4 mb-4">Olá, sou Leandro Campos</h1>
            <p class="lead text-muted mb-5">
                Movido pela curiosidade e fascinado pelo poder da tecnologia em transformar o mundo. 
                Cada projeto é uma nova chance de inovar e criar soluções que fazem a diferença na vida das pessoas.
            </p>
            <div class="button-group">
                <a href="#projetos" class="btn btn-primary me-3">Ver Projetos</a>
                <a href="#contato" class="btn btn-outline-primary me-3">Contato</a>
                <a href="/public/curriculoDev.pdf" 
                   download="Leandro_Campos_CV.pdf"
                   class="btn btn-outline-dark">
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
.profile-img-container {
    width: 400px;
    height: 400px;
    margin: 0 auto;
}

.profile-img-wrapper {
    width: 100%;
    height: 100%;
    overflow: hidden;
    border: 3px solid var(--primary-color);
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

cv-download-btn {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: var(--primary-color);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    transition: all 0.3s ease;
    z-index: 1000;
}

.cv-download-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    background-color: #0056b3;
    color: white;
}

.cv-download-btn i {
    font-size: 24px;
}

.button-group {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 2rem;
}

.lead {
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.8;
}

/* Ajuste responsivo para telas menores */
@media (max-width: 768px) {
    .button-group {
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }

    .button-group .btn {
        width: 200px; /* ou o tamanho que preferir */
        margin: 5px 0;
    }
}

h1 {
    animation: fadeIn 1s ease-out;
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
</style>