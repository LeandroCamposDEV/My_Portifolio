<template>
    <section id="projetos" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-5">Projetos Pessoais</h2>
            <div class="row g-4">
                <div v-for="projeto in projetos" :key="projeto.nome" class="col-md-6 col-lg-4">
                    <div class="card h-100 shadow-sm">
                        <img :src="projeto.imagem" class="card-img-top" :alt="projeto.nome">
                        <div class="card-body">
                            <h5 class="card-title">{{ projeto.nome }}</h5>
                            <p class="card-text">{{ projeto.descricao }}</p>
                            <div class="d-flex flex-wrap gap-2 mb-3">
                                <span v-for="tech in projeto.tecnologias" :key="tech" class="badge bg-light text-dark">
                                    {{ tech }}
                                </span>
                            </div>
                            <a :href="projeto.link" target="_blank" class="btn btn-primary">
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
</style>