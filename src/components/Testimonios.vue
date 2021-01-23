<template>
  <div>
      <div class="row mt-4">
          <div class="col p-0 ">
                <svg class="testimonios-v1 d-none d-sm-block" width="187" height="547" viewBox="0 0 187 547" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M4.02922 538.88C60.2572 505.082 145.064 433.701 58.4307 377.55C-35.7296 316.52 39.9095 239.455 90.5744 217.566C142.325 195.208 171.842 170.331 179.766 149.608C203.522 83.1232 167.969 -57.4236 -9.00003 26.3207L-9.00005 227.057L-9.00011 262.763L-9.00013 317.295L-9.00012 396.614L-9.00014 546.853L4.02922 538.88Z" fill="#FF2C2C"/>
                </svg>
                
          </div>
          <div class="col">
                <div id="carouselExampleSlidesOnly" class="testimonio-slide carousel slide" data-ride="carousel">
                    <div class="carousel-inner">
                        <div v-for="(item,index) in testimonios" :key="index" :class="item.activo === true ? 'carousel-item active' :'carousel-item'">
                            <h1 class="d-block w-100 text-center">"{{item.titulo}}"</h1>
                            <p class="d-block w-100 text-justify text-secondary">{{item.subtitulo}}</p>                            
                        </div>                        
                    </div>
                </div>
          </div>

          <div class="col p-0">                
                <svg class="testimonios-v2 d-none d-sm-block" width="246" height="547" viewBox="0 0 214 547" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M180.734 8.41235C124.506 42.2103 39.6989 113.591 126.332 169.742C220.493 230.772 144.853 307.837 94.1885 329.726C42.4383 352.084 12.9208 376.961 4.99732 397.684C-18.3685 463.075 38.3835 600.109 213.763 524.926V320H223.763V284.529L223.763 229.997L223.763 150.678V0.438904L180.734 8.41235Z" fill="#FF2C2C"/>
                </svg>
                <img class="testimonios-img d-none d-sm-block" src="../assets/imagenes/testimonios/testimonials_bg_ketchup.png" alt="Testimonials">   
          </div>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            testimonios: [
                {titulo:'Es un enfoque diferente', subtitulo:'El cual ayuda a mejorar las organizacines de este rubro a travez de la optimizacion de la planificacion estrategica del negocio.', activo:true},
                {titulo:'Restaurante con identidad', subtitulo:'En seguida me quedé seducido por la decoración, por los platos y por la atención! Un verdadero restaurante catalán! La comida deliciosa y el servicio excelente!', activo:false},
                {titulo:'Para repetir!', subtitulo:'Ya es nuestra segunda vez en este restaurante, la verdad es que no nos ha defraudado en ninguno de los sentidos, platos y servicio exquisitos, para volver una y otra vez.', activo:false},
                {titulo:'Espectacular como siempre', subtitulo:'El carpaccio de buey buenísimo con parmesano y foie. El secreto es la especialidad de la casa. Y el trato familiar, inmejorable.', activo:false}
            ]
        }
    },
}
</script>

<style>
    .testimonios-v1{
        position: absolute;
        top: 100px;
        height: 500px;
    }
    .testimonios-v2{
        position: absolute;        
        left: 250px;
        top: 150px;        
    }
    .testimonios-img{
        position:absolute;
        top: 82px;
        left:32px;
    }
    .testimonio-slide{
        position: absolute;
        top:150px;
    }
</style>