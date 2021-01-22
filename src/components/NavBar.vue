<template>
    <nav :class="scroll_position >= 200 ? 'navbar fixed-top navbar-expand-lg navbar-dark bg-dark' : 'navbar fixed-top navbar-expand-lg navbar-light ' + { 'navbarOpen': show }" id="mynavbar">    
        <div class="container-fluid">
            <a class="navbar-brand" href="/">Foodies</a>
            <button class="navbar-toggler text-secondary" 
                    type="button"
                    data-bs-toggle="collapse"                
                    data-bs-target="#navbarTogglerDemo02" 
                    aria-controls="navbarTogglerDemo02" 
                    aria-expanded="false" 
                    aria-label="Toggle navigation"
                    @click.stop="toggleNavbar()">
                <span class="navbar-toggler-icon"></span>
            </button>           

            <div class="collapse navbar-collapse" id="navbarTogglerDemo02" v-bind:class="{ 'show': show }">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item mx-4">
                        <a class="nav-link" href="#" @click.prevent="scrollToSection('#home')" target="_self">Inicio</a>
                    </li>
                    <li class="nav-item mx-4">
                        <a class="nav-link" href="#" target="_self" @click.prevent="scrollToSection('#acercade')">Acerca de</a>
                    </li>
                    <li class="nav-item mx-4">
                        <a class="nav-link" href="#" target="_self" @click.prevent="scrollToSection('#sucursales')">Restaurantes</a>
                    </li>
                    <li class="nav-item mx-4">
                        <a class="nav-link " href="#" tabindex="-1" >Menu</a>
                    </li>
                    <li class="nav-item mx-4">
                        <a class="nav-link" href="#" @click.prevent="scrollToSection('#contactanos')">Contactanos</a>
                    </li>
                    
                </ul>            
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    props: {
        homePosition: {
            type: Number,
            default: 0 
        },
    },
    data() {
        return {            
            show:false,
            scroll_position: ''          
        }
    },
    created () {
        window.addEventListener('scroll', this.handleScroll);;
    },
    methods: {
        toggleNavbar() {
            this.show = !this.show;
        },
        handleScroll(event){
            let navbar = window.scrollY + document.querySelector('#home').getBoundingClientRect().top; // Y
            let scrollTop = document.documentElement.scrollTop;      
            this.scroll_position = scrollTop;
        },
        scrollToSection(section){
            let element = document.querySelector(section);
            element.scrollIntoView({ behavior: 'smooth'});
        },
        

    },
}
</script>

