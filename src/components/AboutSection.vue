<template>
    <section id="sobre" class="py-5 bg-white">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Sobre Mim</h2>
            <div class="row justify-content-center">
                <div class="col-lg-8">
                    <div class="card border-0 shadow-sm p-4">
                        <div class="journey-section mb-4">
                            <h3 class="h4 mb-3">Minha História</h3>
                            <p class="mb-3">
                                Hey! Sou um entusiasta da tecnologia que decidiu dar uma guinada na carreira pra mergulhar de cabeça no mundo do desenvolvimento. Depois de anos trabalhando em outra área, percebi que minha verdadeira paixão estava em criar soluções digitais que impactam a vida das pessoas.
                            </p>
                            <p>
                                Atualmente, estou focado em me tornar um Engenheiro de Software completo, estudando na Estácio e me especializando em desenvolvimento Front-end na EBAC. Cada dia é uma nova descoberta e cada linha de código é um passo em direção ao meu objetivo!
                            </p>
                        </div>

                        <div class="passions-section mb-4">
                            <h3 class="h4 mb-3">O Que Me Move</h3>
                            <ul class="list-unstyled">
                                <li class="mb-2">
                                    <i class="bi bi-code-slash me-2"></i>
                                    Desenvolvimento Web & Novas Tecnologias
                                </li>
                                <li class="mb-2">
                                    <i class="bi bi-lightbulb me-2"></i>
                                    Solução Criativa de Problemas
                                </li>
                                <li class="mb-2">
                                    <i class="bi bi-graph-up me-2"></i>
                                    Aprendizado Contínuo
                                </li>
                            </ul>
                        </div>

                        <div class="skills-section">
                            <h3 class="h4 mb-3">Soft Skills</h3>
                            <div class="row g-4">
                                <div class="col-md-4">
                                    <div class="skill-card text-center p-3">
                                        <i class="bi bi-people-fill display-6 mb-2 text-primary"></i>
                                        <h4 class="h5">Trabalho em Equipe</h4>
                                        <p class="small text-muted">
                                            Colaboração e troca de ideias. Adoro um bom trabalho em equipe!
                                        </p>
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="skill-card text-center p-3">
                                        <i class="bi bi-chat-dots-fill display-6 mb-2 text-primary"></i>
                                        <h4 class="h5">Comunicação</h4>
                                        <p class="small text-muted">
                                            Transformo conceitos complexos em explicações claras e objetivas.
                                        </p>
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="skill-card text-center p-3">
                                        <i class="bi bi-arrow-up-circle-fill display-6 mb-2 text-primary"></i>
                                        <h4 class="h5">Resiliência</h4>
                                        <p class="small text-muted">
                                            Encaro desafios como oportunidades de crescimento. Bugs? Trago soluções!
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.skill-card {
    transition: transform 0.3s ease;
    border-radius: 8px;
}

.skill-card:hover {
    transform: translateY(-5px);
    background-color: var(--background-light);
}

.journey-section, .passions-section {
    position: relative;
    padding-left: 1rem;
}

.journey-section::before, .passions-section::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 3px;
    background-color: var(--primary-color);
    border-radius: 4px;
}

.bi {
    color: var(--primary-color);
}
</style>