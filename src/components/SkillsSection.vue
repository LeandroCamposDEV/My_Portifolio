<template>
    <section id="stacks" class="min-vh-100 py-5">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Stack em Aprendizado</h2>
            <div class="row g-4 justify-content-center">
                <div v-for="skill in skills" :key="skill.name" class="col-6 col-md-4 col-lg-3">
                    <div class="skill-card">
                        <div class="skill-icon-wrapper">
                            <img :src="skill.icon" :alt="skill.name" class="skill-icon">
                        </div>
                        <h5 class="skill-title">{{ skill.name }}</h5>
                        <div class="progress-wrapper">
                            <div class="progress">
                                <div class="progress-bar" 
                                     role="progressbar" 
                                     :style="{ width: skill.level + '%' }"
                                     :aria-valuenow="skill.level" 
                                     aria-valuemin="0" 
                                     aria-valuemax="100">
                                </div>
                            </div>
                            <span class="progress-label">{{ getSkillLevel(skill.level) }}</span>
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
    methods: {
        getSkillLevel(level) {
            if (level < 30) return 'Iniciante'
            if (level < 60) return 'Intermediário'
            return 'Avançado'
        }
    },
    data() {
        return {
            skills: [
                { name: 'JavaScript', icon: '/skills/javascript-1.svg', level: 50 },
                { name: 'Python', icon: '/skills/python-5.svg', level: 20 },
                { name: 'Bootstrap', icon: '/skills/bootstrap-5-1.svg', level: 50 },
                { name: 'Sass', icon: '/skills/sass-1.svg', level: 35 },
                { name: 'Vue', icon: '/skills/vue-9.svg', level: 40 },
                { name: 'React', icon: '/skills/react-2.svg', level: 40 },
                { name: 'Azure IA', icon: '/skills/azure-2.svg', level: 20 },
                { name: 'PostgreSQL', icon: '/skills/postgresql.svg', level: 20 }
            ]
        }
    }
}
</script>

<style scoped>
section {
    background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
    padding-top: 80px;
}

h2 {
    color: #2d2d2d;
    font-weight: 700;
    margin-bottom: 3rem;
}

.skill-card {
    background: white;
    border-radius: 15px;
    padding: 2rem 1.5rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.skill-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
}

.skill-icon-wrapper {
    width: 80px;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1.5rem;
    border-radius: 50%;
    background: rgba(155, 93, 229, 0.1);
    padding: 1rem;
}

.skill-icon {
    width: 100%;
    height: 100%;
    object-fit: contain;
    transition: transform 0.3s ease;
}

.skill-card:hover .skill-icon {
    transform: scale(1.1);
}

.skill-title {
    font-size: 1.1rem;
    font-weight: 600;
    color: #2d2d2d;
    margin-bottom: 1.5rem;
    text-align: center;
}

.progress-wrapper {
    width: 100%;
}

.progress {
    height: 8px;
    background-color: #f0f0f0;
    border-radius: 10px;
    overflow: hidden;
    margin-bottom: 0.5rem;
}

.progress-bar {
    background: linear-gradient(135deg, #9b5de5 0%, #00bbf9 100%);
    transition: width 1s ease;
}

.progress-label {
    font-size: 0.85rem;
    color: #666;
    font-weight: 500;
}

@media (max-width: 768px) {
    section {
        padding-top: 60px;
    }
    
    .skill-card {
        padding: 1.5rem 1rem;
    }
    
    .skill-icon-wrapper {
        width: 60px;
        height: 60px;
    }
}
</style>