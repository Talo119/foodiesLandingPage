<template>
    <div>
        <div class="row">
            <div class="col-sm-7">
                <img class="acercade-img" src="../assets/imagenes/acercade/linear_bg.png" alt="">
                <img class="acercade-img" src="../assets/imagenes/acercade/aGZeHyx-jfo.png" alt="">
                <img class="comida-img" src="../assets/imagenes/acercade/LA COMIDA ES NUESTRO ARTE.png" alt="">
            </div>
            <div class="col-sm-5">
                <svg class="v3" width="830" height="352" viewBox="0 0 830 352" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M0.624512 217.704C112.447 209.842 178.953 117.622 276.688 76.0659C361.139 40.1576 428.335 67.254 429.675 161.049C430.48 217.444 413.658 268.76 373.283 309.813C254.83 430.258 192.331 252.3 299.737 179.875C369.258 132.997 461.374 192.146 531.813 204.332C644.917 223.9 767.344 216.36 786.586 78.0014C794.494 21.1398 725.228 -9.9287 680.313 26.7124C580.132 108.44 598.746 279.748 745.766 244.009C857.412 216.868 931.94 102.993 1013.56 29.1757C1022.39 21.1931 1039.13 0.76001 1052.09 0.76001" stroke="#FFD600" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <h6 class="title-acercade">Quien es Foodies?</h6>
                <p class="parrafo-acercade">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Possimus officiis error laborum magni recusandae? Quos, mollitia nostrum voluptatibus quas vitae est consequatur in fugiat a tempora molestias minus illo autem!</p>
                <h5>
                    <a class="txt-contactanos ml-0 pl-0"  href="#">
                        Contáctanos
                        <img class="v-flecha1" src="../assets/imagenes/Flecha1.png" alt="">
                        <img class="v-flecha2" src="../assets/imagenes/Flecha2.png" alt="">
                    </a>
                </h5>
                
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
    .acercade-img{
        position: absolute;
        width: 816px;
        height: 565px;
        left: 0px;
        top: 50px;

        background: url(../assets/imagenes/acercade/aGZeHyx-jfo.png);
    }
    .comida-img{
        position: absolute;
        width: 579px;
        height: 100px;
        left: 197px;
        top: 450px;
    }
    .v3{
        position: absolute;
        width: 600px;
        height: 349.79px;
        left: 1px;
        top: 150px;

        border: 0px solid #FFD600;
    }
    .title-acercade{
        position: absolute;
        width: 234px;
        height: 27px;
        left: 10px;
        top: 240px;
    }
    .parrafo-acercade{
        position: absolute;
        width: 570px;
        height: 99px;
        left: 10px;
        top: 270px;
        color: rgba(0, 0, 0, 0.4);
    }
    .txt-contactanos{
        position: absolute;
        width: 570px;
        height: 99px;
        left: 10px;
        top: 400px;
        color: #000000;
    }
    .v-flecha1{
        position: absolute;                        
        width: 14px;
        left: 130px;
        top: 15px;        
        border: 0px solid #000000;
    }
    .v-flecha2{
        position: absolute;
        height: 14px;
        width: 7px;
        left: 140px;
        top: 9px;
        border-radius: 0px;
        border: 0px solid #000000;
    }    
</style>