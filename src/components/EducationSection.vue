<template>
    <section id="educacao" class="min-vh-100 py-5">
        <div class="container">
            <h2 class="text-center display-5 mb-5">Educação</h2>
            <div class="row g-4">
                <div v-for="edu in education" :key="edu.course" class="col-md-6">
                    <div class="education-card">
                        <div class="row g-0 align-items-center">
                            <div class="col-4">
                                <div class="logo-wrapper">
                                    <img :src="edu.logo" class="institution-logo" :alt="edu.institution">
                                </div>
                            </div>
                            <div class="col-8">
                                <div class="card-content">
                                    <h5 class="education-title">{{ edu.course }}</h5>
                                    <p class="institution-name">{{ edu.institution }}</p>
                                    <span class="status-badge">{{ edu.status }}</span>
                                </div>
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
    name: 'EducationSection',
    data() {
        return {
            education: [
                {
                    course: 'Bacharelado em Engenharia de Software',
                    institution: 'Estácio',
                    status: 'Cursando',
                    logo: '/education/estacio.jpg'
                },
                {
                    course: 'Engenheiro FrontEnd',
                    institution: 'EBAC',
                    status: 'Cursando',
                    logo: '/education/ebac.jpg'
                },
                {
                    course: 'Get Fluent Método ACT',
                    institution: 'Professor Junior Silveira',
                    status: 'Cursando',
                    logo: '/education/english.jpg'
                },
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

.education-card {
    background: white;
    border-radius: 15px;
    padding: 1.5rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
    height: 100%;
}

.education-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
}

.logo-wrapper {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1rem;
}

.institution-logo {
    width: 100%;
    height: auto;
    object-fit: contain;
    transition: transform 0.3s ease;
}

.education-card:hover .institution-logo {
    transform: scale(1.05);
}

.card-content {
    padding-left: 1rem;
}

.education-title {
    color: #2d2d2d;
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 0.5rem;
    line-height: 1.4;
}

.institution-name {
    color: #666;
    font-size: 0.95rem;
    margin-bottom: 0.75rem;
}

.status-badge {
    display: inline-block;
    padding: 0.35rem 0.75rem;
    background: rgba(155, 93, 229, 0.1);
    color: #9b5de5;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
}

@media (max-width: 768px) {
    section {
        padding-top: 60px;
    }
    
    .education-card {
        padding: 1rem;
    }
    
    .card-content {
        padding-left: 0.5rem;
    }
    
    .education-title {
        font-size: 1rem;
    }
}
</style>