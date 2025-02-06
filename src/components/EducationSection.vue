<template>
    <section id="educacao" class="py-5 bg-white">
        <div class="container">
            <h2 class="text-center mb-5">Educação</h2>
            <div class="row g-4">
                <div v-for="edu in education" :key="edu.course" class="col-md-6">
                    <div class="card h-100 border-0 shadow-sm">
                        <div class="row g-0">
                            <div class="col-4">
                                <img :src="edu.logo" class="img-fluid p-3" :alt="edu.institution">
                            </div>
                            <div class="col-8">
                                <div class="card-body">
                                    <h5 class="card-title">{{ edu.course }}</h5>
                                    <p class="card-text">{{ edu.institution }}</p>
                                    <p class="card-text"><small class="text-muted">{{ edu.status }}</small></p>
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