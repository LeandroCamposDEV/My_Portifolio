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
                                Plot twist profissional! Em um capítulo anterior da minha vida, trabalhei em outra área completamente diferente. Mas a tecnologia sempre foi aquele chamado persistente, até que um dia, aos 35 anos, decidi ouvir. Essa coragem de recomeçar me trouxe até aqui: estudante de Engenharia de Software com um olhar diferenciado sobre problemas e soluções. Com a maturidade de quem já navegou pelas complexidades da vida profissional, trago para o código a serenidade para enfrentar desafios e a sabedoria para priorizar o que realmente importa. Carrego comigo a determinação de quem sabe o valor de construir algo novo e a experiência diversificada que me permite conectar mundos. Enquanto muitos trazem apenas conhecimento técnico, ofereço algo mais valioso: perspectiva. Cada linha de código que escrevo carrega essa história de transformação, propósito e a rica bagagem de quem não tem medo de evoluir, não importa o momento da vida.
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