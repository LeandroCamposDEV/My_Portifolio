<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Leandro Campos</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li v-for="item in menuItems" :key="item.href" class="nav-item">
                        <a class="nav-link" :href="item.href">{{ item.text }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'HeaderSection',
    data() {
        return {
            menuItems: [
                { href: '#inicio', text: 'Início' },
                { href: '#sobre', text: 'Sobre' },
                { href: '#projetos', text: 'Projetos' },
                { href: '#stacks', text: 'Stacks' },
                { href: '#certificados', text: 'Certificados' },
                { href: '#educacao', text: 'Educação' },
                { href: '#objetivos', text: 'Objetivos' },
                { href: '#contato', text: 'Contato' }
            ]
        }
    }
}
</script>

<style scoped>
.navbar {
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.nav-link {
    transition: color 0.3s ease;
}

.nav-link:hover {
    color: var(--primary-color) !important;
}
</style>