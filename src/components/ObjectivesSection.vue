<template>
    <section id="objetivos" class="min-vh-100 py-5">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Objetivos Profissionais</h2>
            <div class="row justify-content-center">
                <div class="col-md-6">
                    <div class="objectives-card mb-4">
                        <h3 class="card-title">
                            <i class="bi bi-rocket-takeoff"></i>
                            Curto Prazo
                        </h3>
                        <ul class="goals-list">
                            <li v-for="(goal, index) in shortTermGoals" 
                                :key="index" 
                                class="goal-item">
                                <i class="bi bi-check-circle-fill"></i>
                                <span>{{ goal }}</span>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="objectives-card">
                        <h3 class="card-title">
                            <i class="bi bi-stars"></i>
                            Longo Prazo
                        </h3>
                        <ul class="goals-list">
                            <li v-for="(goal, index) in longTermGoals" 
                                :key="index" 
                                class="goal-item">
                                <i class="bi bi-star-fill"></i>
                                <span>{{ goal }}</span>
                            </li>
                        </ul>
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

.objectives-card {
    background: rgba(255, 255, 255, 0.95);
    border-radius: 15px;
    padding: 2rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
    transition: all 0.3s ease;
    height: 100%;
}

.objectives-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
}

.card-title {
    color: #1e3a8a;
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
}

.card-title i {
    color: #00bbf9;
    font-size: 1.75rem;
}

.goals-list {
    list-style: none;
    padding: 0;
    margin: 0;
}

.goal-item {
    display: flex;
    align-items: flex-start;
    gap: 1rem;
    padding: 1rem;
    margin-bottom: 0.5rem;
    border-radius: 10px;
    transition: all 0.3s ease;
}

.goal-item:hover {
    background: rgba(0, 187, 249, 0.1);
    transform: translateX(5px);
}

.goal-item i {
    color: #00bbf9;
    font-size: 1.2rem;
    flex-shrink: 0;
}

.goal-item span {
    color: #4a5568;
    font-size: 1rem;
    line-height: 1.5;
}

@media (max-width: 768px) {
    section {
        padding-top: 60px;
    }

    .objectives-card {
        padding: 1.5rem;
        margin-bottom: 1rem;
    }

    .card-title {
        font-size: 1.25rem;
    }

    .goal-item {
        padding: 0.75rem;
    }
}

@media (max-width: 375px) {
    .objectives-card {
        padding: 1rem;
    }

    .card-title {
        font-size: 1.1rem;
    }

    .goal-item {
        padding: 0.5rem;
        font-size: 0.9rem;
    }

    .goal-item i {
        font-size: 1rem;
    }
}
</style>