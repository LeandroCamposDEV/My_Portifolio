<template>
    <section id="sobre" class="min-vh-100 d-flex align-items-center position-relative">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Sobre Mim</h2>
            <div class="row justify-content-center">
                <div class="col-lg-8">
                    <div class="about-card p-4">
                        <div class="journey-section mb-5">
                            <h3 class="h4 mb-4">Minha História</h3>
                            <p class="lead">
                                Hey! Sou um entusiasta da tecnologia que decidiu dar uma guinada na carreira pra mergulhar de cabeça no mundo do desenvolvimento. Depois de anos trabalhando em outra área, percebi que minha verdadeira paixão estava em criar soluções digitais que impactam a vida das pessoas.
                            </p>
                            <p class="lead">
                                Atualmente, estou focado em me tornar um Engenheiro de Software completo, estudando na Estácio e me especializando em desenvolvimento Front-end na EBAC. Cada dia é uma nova descoberta e cada linha de código é um passo em direção ao meu objetivo!
                            </p>
                        </div>

                        <div class="skills-grid mt-5">
                            <div class="skill-item">
                                <div class="skill-icon">
                                    <i class="bi bi-people-fill"></i>
                                </div>
                                <h4>Trabalho em Equipe</h4>
                                <p>Colaboração e troca de ideias</p>
                            </div>
                            <div class="skill-item">
                                <div class="skill-icon">
                                    <i class="bi bi-chat-dots-fill"></i>
                                </div>
                                <h4>Comunicação</h4>
                                <p>Clareza e objetividade</p>
                            </div>
                            <div class="skill-item">
                                <div class="skill-icon">
                                    <i class="bi bi-arrow-up-circle-fill"></i>
                                </div>
                                <h4>Resiliência</h4>
                                <p>Desafios como oportunidades</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
section {
    background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
    overflow: hidden;
}

.container {
    position: relative;
    z-index: 2;
}

.about-card {
    background: rgba(255, 255, 255, 0.9);
    border-radius: 20px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}

.about-card:hover {
    transform: translateY(-5px);
}

.lead {
    font-size: 1.1rem;
    line-height: 1.8;
    color: #4a4a4a;
    margin-bottom: 1.5rem;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
    padding: 2rem 0;
}

.skill-item {
    text-align: center;
    padding: 1.5rem;
    background: white;
    border-radius: 15px;
    transition: all 0.3s ease;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

.skill-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.skill-icon {
    width: 60px;
    height: 60px;
    margin: 0 auto 1rem;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, #9b5de5 0%, #00bbf9 100%);
    border-radius: 50%;
}

.skill-icon i {
    font-size: 1.5rem;
    color: white;
}

h2 {
    color: #2d2d2d;
    font-weight: 700;
    margin-bottom: 2rem;
}

@media (max-width: 768px) {
    .skills-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
    }
    
    .lead {
        font-size: 1rem;
    }
}
</style>