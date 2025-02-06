<template>
    <section id="objetivos" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-5">Objetivos Profissionais</h2>
            <div class="row justify-content-center">
                <div class="col-md-8">
                    <div class="card shadow-sm">
                        <div class="card-body p-4">
                            <h3 class="h4 mb-4">Curto Prazo</h3>
                            <ul class="list-unstyled mb-5">
                                <li v-for="(goal, index) in shortTermGoals" 
                                    :key="index" 
                                    class="mb-3 d-flex align-items-center">
                                    <i class="bi bi-check-circle-fill text-primary me-3"></i>
                                    {{ goal }}
                                </li>
                            </ul>

                            <h3 class="h4 mb-4">Longo Prazo</h3>
                            <ul class="list-unstyled">
                                <li v-for="(goal, index) in longTermGoals" 
                                    :key="index" 
                                    class="mb-3 d-flex align-items-center">
                                    <i class="bi bi-star-fill text-primary me-3"></i>
                                    {{ goal }}
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ObjectivesSection',
    data() {
        return {
            shortTermGoals: [
                'Desenvolver projetos full-stack mais complexos',
                'Aprofundar conhecimentos em Vue.js e React',
                'Desenvolver habilidades em Cloud Computing e DevOps'
            ],
            longTermGoals: [
                'Especializar-me em Inteligência Artificial e Machine Learning',
                'Liderar equipes de desenvolvimento',
                'Criar soluções inovadoras que impactem positivamente a sociedade'
            ]
        }
    }
}
</script>

<style scoped>
.card {
    border-radius: 15px;
    border: none;
}

.card-body {
    position: relative;
}

.bi-check-circle-fill {
    font-size: 1.2rem;
    color: #0d6efd;
}

.bi-star-fill {
    font-size: 1.2rem;
    color: #0d6efd;
}

li {
    font-size: 1.1rem;
    transition: transform 0.2s ease;
}

li:hover {
    transform: translateX(5px);
}

@media (max-width: 768px) {
    li {
        font-size: 1rem;
    }
}
</style>