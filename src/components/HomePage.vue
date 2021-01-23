<template>
    <div>            
        <div class="row">
            <div class="col-md-6">
                <img class="bg-text-sm d-block d-sm-none" src="../assets/imagenes/bg_text-sm.png" alt="bg">              
                <img class="bg-text d-none d-sm-block" src="../assets/imagenes/bg_text.png" alt="bg">
                <img class="img-fluid-sm d-block d-sm-none" src="../assets/imagenes/Un nuevo sabor esta en la ciudad-sm.png" alt="Un nuevo sabor">
                <img class="img-fluid d-none d-sm-block mt-5 ml-2" src="../assets/imagenes/Un nuevo sabor esta en la ciudad.png" alt="Un nuevo sabor">
                <h6 class="lema-sm d-block d-sm-none">Estamos a punto de descubrir un mundo lleno de sabores y de emociones inigualables</h6>
                <h6 class="lema d-none d-sm-block">Estamos a punto de descubrir un mundo lleno de sabores y de emociones inigualables</h6>   
                <h4>
                    <a class="txt-encuentranos-sm d-block d-sm-none  ml-0 pl-0"  href="#">
                        Encuentranos
                        <img class="v-f1" src="../assets/imagenes/Flecha1.png" alt="">
                        <img class="v-f2" src="../assets/imagenes/Flecha2.png" alt="">
                    </a>                    
                </h4>
                <h4>
                    <a class="txt-encuentranos d-none d-sm-block ml-0 pl-0"  href="#">
                        Encuentranos
                        <img class="v-f1" src="../assets/imagenes/Flecha1.png" alt="">
                        <img class="v-f2" src="../assets/imagenes/Flecha2.png" alt="">
                    </a>                    
                </h4>
                
            </div>
            <div class="col-md-6">
                <svg class="d-block d-sm-none" width="366" height="395" viewBox="0 0 366 395" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M119.693 -97.1324C71.6077 -59.1653 1.51406 16.9804 88.5025 58.6302C183.049 103.899 122.13 184.214 77.7809 210.499C32.4819 237.347 8.08931 263.88 3.21578 283.999C-12.7044 356.689 24.172 469.454 258.101 325.374C313.206 291.434 353.131 270.153 381.328 258.234V67.6818H392.611V-102H119.693V-97.1324Z" fill="#FFD600"/>
                </svg>              
                <svg class="d-none d-sm-block" width="744" height="794" viewBox="0 0 792 794" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M246.026 -218C147.187 -140 3.11211 16.4343 181.914 102C376.252 195 251.035 360 159.876 414C66.7656 469.157 16.6274 523.667 6.60995 565C-26.1136 714.333 49.6849 946 530.52 650C650.168 576.345 734.999 531.709 793.378 508.112V-40H807V-228H246.026V-218Z" fill="#FFD600"/>
                </svg>
                <img class="hero-hamburger-sm d-block d-sm-none" src="../assets/imagenes/hero_hamburger-sm.png" alt="Hero Hamburguer">
                <img class="hero-hamburger d-none d-sm-block" src="../assets/imagenes/hero_hamburger.png" alt="Hero Hamburguer">
                
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
    .img-fluid-sm {
        position: absolute;
        width: 343px;
        height: 105px;
        left: 10px;
        top: 400px;
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
    .bg-text-sm {
        position: absolute;
        width: 242.66px;
        height: 54px;
        left: 10px;
        top: 460px;
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
    .hero-hamburger-sm{
        position: absolute;
        width: 312.93px;
        height: 246px;
        top: 100px;
        left:30px;
        
    }
    .lema{
        position: absolute;
        width: 498px;
        height: 50px;
        left: 102px;
        top: 468px;
        color:rgba(0, 0, 0, 0.4)
    }
    .lema-sm{
        position: absolute;
        width: 300px;
        height: 50px;
        left: 10px;
        top: 520px;
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
    .txt-encuentranos-sm{
        position: absolute;
        width: 182px;
        height: 27px;
        left: 102px;
        top: 595px;
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