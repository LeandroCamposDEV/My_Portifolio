<template>
    <nav class="navbar navbar-expand-lg fixed-top">
        <div class="container">
            <button class="navbar-toggler order-0" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse order-2" id="navbarNav">
                <ul class="navbar-nav mx-auto">
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
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
    padding: 1rem 0;
    transition: all 0.3s ease;
}

.navbar-brand {
    font-weight: 700;
    font-size: 1.5rem;
    color: #2d2d2d;
    transition: all 0.3s ease;
    margin-right: 0; /* Remove default margin */
}

.brand-text {
    background: linear-gradient(135deg, #9b5de5 0%, #00bbf9 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 1.8rem; /* Increased font size */
    letter-spacing: 1px; /* Added letter spacing */
}

.navbar-brand:hover {
    transform: translateY(-2px);
}

.nav-link {
    color: #4a4a4a !important;
    font-weight: 500;
    padding: 0.5rem 1rem !important;
    margin: 0 0.2rem;
    border-radius: 25px;
    transition: all 0.3s ease;
}

.nav-link:hover {
    color: #9b5de5 !important;
    background: rgba(155, 93, 229, 0.1);
    transform: translateY(-2px);
}

.navbar-toggler {
    border: none;
    padding: 0.5rem;
}

.navbar-toggler:focus {
    box-shadow: none;
    outline: none;
}

@media (max-width: 991px) {
    .navbar-brand {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
    }
    
    .navbar-toggler {
        margin-left: 1rem;
    }

    .navbar-nav {
        padding: 1rem 0;
        text-align: center;
    }

    .nav-link {
        padding: 0.8rem 1rem !important;
        text-align: center;
    }

    .nav-link:hover {
        background: rgba(155, 93, 229, 0.1);
    }
}
</style>