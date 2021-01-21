<template>
    <div>            
        <div class="row">
            <div class="col-md-6">
                <img class="bg-text" src="../assets/imagenes/bg_text.png" alt="bg">
                <img class="img-fluid mt-5 ml-2" src="../assets/imagenes/Un nuevo sabor esta en la ciudad.png" alt="Un nuevo sabor">
                <h6 class="lema">Estamos a punto de descubrir un mundo lleno de sabores y de emociones inigualables</h6>   
                <h4>
                    <a class=" txt-encuentranos ml-0 pl-0"  href="#">
                        Encuentranos
                        <img class="v-f1" src="../assets/imagenes/Flecha1.png" alt="">
                        <img class="v-f2" src="../assets/imagenes/Flecha2.png" alt="">
                    </a>                    
                </h4>
                
            </div>
            <div class="col-md-6">                
                <svg width="792" height="794" viewBox="0 0 792 794" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M246.026 -218C147.187 -140 3.11211 16.4343 181.914 102C376.252 195 251.035 360 159.876 414C66.7656 469.157 16.6274 523.667 6.60995 565C-26.1136 714.333 49.6849 946 530.52 650C650.168 576.345 734.999 531.709 793.378 508.112V-40H807V-228H246.026V-218Z" fill="#FFD600"/>
                </svg>
                <img class="hero-hamburger" src="../assets/imagenes/hero_hamburger.png" alt="Hero Hamburguer">
                
            </div>
        </div>  
    </div>
    
    
</template>

<script>
import NavBar from '../components/NavBar'
export default {
    components: {
        NavBar,
    },
    data() {
        return {
            navBarPosition: 0
        }
    },
    methods: {
        
    },
}
</script>

<style>
    .img-fluid {
        position: absolute;
        width: 579px;
        height: 180px;
        left: 102px;
        top: 225px;
    }
    .bg-text {
        position: absolute;
        width: 411px;
        height: 54px;
        left: 88.71px;
        top: 395.3px;
        background: #FFD600;
        transform: rotate(-0.64deg);
    }
    .hero-hamburger{
        position: absolute;
        height: 446.26416015625px;
        width: 567px;
        left: 135px;
        top: 161.991943359375px;
        border-radius: 0px;
        background: url('../assets/imagenes/hero_hamburger.png');

    }
    .lema{
        position: absolute;
        width: 498px;
        height: 50px;
        left: 102px;
        top: 468px;
        color:rgba(0, 0, 0, 0.4)
    }
    .txt-encuentranos{
        position: absolute;
        width: 182px;
        height: 27px;
        left: 102px;
        top: 564px;
        color: #000000;
    }
    .miboton{
        position: absolute;
        top:600px;
    }
    .v-f1{
        position: absolute;                        
        width: 14px;
        left: 170px;
        top: 15px;        
        border: 0px solid #000000;
    }
    .v-f2{
        position: absolute;
        height: 14px;
        width: 7px;
        left: 180px;
        top: 9px;
        border-radius: 0px;
        border: 0px solid #000000;
    }
    
</style>