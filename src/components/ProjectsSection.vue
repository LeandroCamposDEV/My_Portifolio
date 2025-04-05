<template>
    <section id="projetos" class="min-vh-100 py-5">
        <div class="container">
            <h2 class="text-center display-4 mb-5">Projetos Pessoais</h2>
            <div class="row g-4">
                <div v-for="projeto in projetos" :key="projeto.nome" class="col-md-6 col-lg-4">
                    <div class="project-card h-100">
                        <div class="card-image-wrapper">
                            <img :src="projeto.imagem" class="card-img-top" :alt="projeto.nome">
                        </div>
                        <div class="card-body">
                            <h5 class="card-title">{{ projeto.nome }}</h5>
                            <p class="card-text">{{ projeto.descricao }}</p>
                            <div class="tech-stack mb-3">
                                <span v-for="tech in projeto.tecnologias" 
                                      :key="tech" 
                                      class="tech-badge">
                                    {{ tech }}
                                </span>
                            </div>
                            <a :href="projeto.link" 
                               target="_blank" 
                               class="btn btn-modern">
                                Ver Projeto
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
    name: 'ProjectsSection',
    data() {
        return {
            projetos: [
            {
                    nome: 'Calculadora de IMC',
                    descricao: 'Aplicação de Calculo de IMC com React.js',
                    tecnologias: ['HTML', 'JavaScript', 'React'],
                    link: 'https://calculadora-imc-omega-eight.vercel.app/',
                    imagem: '/projects/imc.jpg'
                },
            {
                    nome: 'Listas de Tarefas',
                    descricao: 'Aplicação web TODO list com Vue.js',
                    tecnologias: ['HTML', 'JavaScript', 'Vue'],
                    link: 'https://todo-vue-puce-nine.vercel.app/',
                    imagem: '/projects/listas_tarefas.jpg'
                },
            {
                    nome: 'Peaky Blinders FanClub',
                    descricao: 'Aplicação web para um fanclub ficticio da série Peaky Blinders',
                    tecnologias: ['HTML', 'JavaScript', 'SASS'],
                    link: 'https://projeto-peaky-blinders.vercel.app/',
                    imagem: '/projects/peaky_blinders.jpg'
                },
              {
                    nome: 'Homestead Bakery',
                    descricao: 'Aplicação web para uma padaria ficticia em Londres',
                    tecnologias: ['HTML', 'CSS'],
                    link: 'https://homestead-bakery.vercel.app/',
                    imagem: '/projects/homestead.jpg'
                },
                {
                    nome: 'Disney Plus',
                    descricao: 'Aplicação web clone Disney Plus',
                    tecnologias: ['HTML', 'JavaScript', 'SASS'],
                    link: 'https://clone-disneyplus-o5vs.vercel.app/',
                    imagem: '/projects/disney+.jpg'
                },
                {
                    nome: 'Sorteador de Números',
                    descricao: 'Aplicação web para sortear números aleatórios',
                    tecnologias: ['HTML', 'JavaScript', 'LESS'],
                    link: 'https://sorteadorgruntleandro-ashy.vercel.app/',
                    imagem: '/projects/sorteador.jpg'
                },
                {
                    nome: 'Agenda de contatos',
                    descricao: 'Aplicação web para gerenciamento de contatos pessoais',
                    tecnologias: ['HTML', 'CSS', 'JavaScript'],
                    link: 'https://leandro-agenda-de-contatos.vercel.app/',
                    imagem: '/projects/agenda.jpg'
                },
                {
                    nome: 'Calculadora de Médias',
                    descricao: 'Ferramenta para cálculo de médias escolares',
                    tecnologias: ['HTML', 'CSS', 'JavaScript'],
                    link: 'https://leandro-projeto-calculadora-medias-eight.vercel.app/',
                    imagem: '/projects/calculadora.jpg'
                },
            ]
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

.project-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
    transition: all 0.3s ease;
    border: none;
}

.project-card:hover {
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

.project-card:hover .card-img-top {
    transform: scale(1.05);
}

.card-body {
    padding: 1.5rem;
}

.card-title {
    color: #1e3a8a;
    font-size: 1.25rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.card-text {
    color: #4a5568;
    font-size: 0.95rem;
    line-height: 1.6;
    margin-bottom: 1.5rem;
}

.tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
}

.tech-badge {
    background: rgba(0, 187, 249, 0.1);
    color: #00bbf9;
    padding: 0.35rem 0.75rem;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
}

.btn-modern {
    background: linear-gradient(135deg, #00bbf9 0%, #1e3a8a 100%);
    color: white;
    border: none;
    padding: 0.75rem 1.5rem;
    border-radius: 25px;
    transition: all 0.3s ease;
    width: 100%;
}

.btn-modern:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(0, 187, 249, 0.3);
}

@media (max-width: 768px) {
    section {
        padding-top: 60px;
    }
    
    .project-card {
        margin-bottom: 1rem;
    }
    
    .card-image-wrapper {
        height: 180px;
    }
    
    h2 {
        font-size: 2rem;
    }
}

@media (max-width: 375px) {
    .card-body {
        padding: 1rem;
    }
    
    .card-title {
        font-size: 1.1rem;
    }
    
    .card-text {
        font-size: 0.9rem;
    }
    
    .tech-badge {
        font-size: 0.8rem;
        padding: 0.25rem 0.6rem;
    }
}
</style>