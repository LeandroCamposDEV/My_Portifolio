<template>
    <section id="stacks" class="py-5 bg-white">
        <div class="container">
            <h2 class="text-center mb-5">Stack em Aprendizado</h2>
            <div class="row g-4 justify-content-center">
                <div v-for="skill in skills" :key="skill.name" class="col-6 col-md-4 col-lg-3">
                    <div class="card h-100 border-0 shadow-sm text-center p-3">
                        <img :src="skill.icon" :alt="skill.name" class="skill-icon mx-auto mb-3">
                        <h5 class="card-title h6">{{ skill.name }}</h5>
                        <div class="progress mt-2">
                            <div class="progress-bar" role="progressbar" :style="{ width: skill.level + '%' }"
                                :aria-valuenow="skill.level" aria-valuemin="0" aria-valuemax="100">
                                Iniciante
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SkillsSection',
    data() {
        return {
            skills: [
                { name: 'JavaScript', icon: '/skills/javascript-1.svg', level: 60 },
                { name: 'Python', icon: '/skills/python-5.svg', level: 30 },
                { name: 'Bootstrap', icon: '/skills/bootstrap-5-1.svg', level: 50 },
                { name: 'Sass', icon: '/skills/sass-1.svg', level: 35 },
                { name: 'Vue', icon: '/skills/vue-9.svg', level: 60 },
                { name: 'React', icon: '/skills/react-2.svg', level: 60 },
                { name: 'Azure IA', icon: '/skills/azure-2.svg', level: 20 },
                { name: 'PostgreSQL', icon: '/skills/postgresql.svg', level: 20 }
            ]
        }
    }
}
</script>

<style scoped>
.skill-icon {
    width: 60px;
    height: 60px;
    object-fit: contain;
}

.card {
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
}
</style>