<template>
  <div>
      <div class="row">
          <div class="col-md-8">
              <h4 class="f-title-sm d-block d-sm-none">Foodies</h4>
              <h4 class="f-title d-none d-sm-block">Foodies</h4>
          </div>
          <div class="col-md-4">
              <img class="img-1-sm d-block d-sm-none mr-2" src="../assets/imagenes/footer/image 1-sm.png" alt="App Store">
              <img class="img-1 d-none d-sm-block mr-2" src="../assets/imagenes/footer/image 1.png" alt="App Store">

              <img class="img-2-sm d-block d-sm-none" src="../assets/imagenes/footer/image 2-sm.png" alt="Google Play">
              <img class="img-2 d-none d-sm-block" src="../assets/imagenes/footer/image 2.png" alt="Google Play">
          </div>
      </div>
      <div class="row">
          <div class="col-12">            
            <svg class="footerv-sm d-block d-sm-none" width="343" height="1" viewBox="0 0 343 1" fill="none" xmlns="http://www.w3.org/2000/svg">
                <line x1="-4.37114e-08" y1="0.5" x2="343" y2="0.49997" stroke="#FFC700"/>
            </svg>
            <svg class="d-none d-sm-block" width="1397" height="1" viewBox="0 0 1397 1" fill="none" xmlns="http://www.w3.org/2000/svg">
                <line y1="0.5" x2="1397" y2="0.5" stroke="#FFC700"/>
            </svg>
          </div>
      </div>
      <div class="row mt-2 mb-2">
          
        <div class="col-md-3 text-center">
            <a class="text-secondary" href="">Conoce nuestras sucursales</a>
        </div>
        <div class="col-md-3 text-center">
            <a class="text-secondary" href="">Acerca de</a>
        </div>
        <div class="col-md-3 text-center">
            <a class="text-secondary" href="">Que hablan de nosotros?</a>
        </div>
        <div class="col-md-3 text-center">
            <a class="text-secondary" href="">Contactanos</a>
        </div>          
          
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
    .img-1{
        position: absolute;
        bottom: 0px;
        left: 210px;
    }
    .img-1-sm{
        position: absolute;
        top: 750px;
        left: 30px;
    }
    .img-2{
        position: absolute;
        bottom: 0px;
    }
    .img-2-sm{
        position: absolute;
        top: 750px;
        left: 210px;
    }    
    .f-title-sm{
        position: absolute;
        top: 650;
    }
    .footerv-sm{
        position: absolute;
        top: 800px;
        left: 0px;
    }
    .f-links-sm{
        position: absolute;
        top: 820px;
    }
</style>