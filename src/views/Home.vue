<template>

  <div class="container-fluid">
    <!-- INICIO -->
    <section id="home" class="home">   
      <HomePage/>      
    </section>
    <!-- ACERCA DE -->
    <section id="acercade" class="acercade">      
      <AcercaDe/>      
    </section>
    <!-- SUCURSALES -->
    <section id="sucursales" class="mx-0 px-0">
      <Sucursales/>
    </section>
    <!-- TESTIMONIOS -->
    <section id="testimonios" class="testimonios">
      <Testimonios/>
    </section>
    <!-- TESTIMONIOS -->
    <section id="contactanos" class="bg-dark">
      <Contactanos/>
    </section>
    <!-- BENEFICIOS -->
    <section id="beneficios">
      <Beneficios/>
    </section>
  </div>
  
</template>

<script>
// @ is an alias to /src
import HomePage from '../components/HomePage'
import AcercaDe from '../components/AcercaDe'
import Sucursales from '../components/Sucursales'
import Testimonios from '../components/Testimonios'
import Contactanos from '../components/Contactanos'
import Beneficios from '../components/Beneficios'


export default {
  name: 'Home',
  components: {
    HomePage, AcercaDe,Sucursales, Testimonios,Contactanos, Beneficios
  },
  data() {
    return {
      
    }
  },
  
  computed: {
    

  },
  methods: {    
    
  },
}
</script>
<style>
  .acercade{
    height: 650px;
  }
  .testimonios{
    height: 650px;
  }
  .contactanos{
    position: absolute;
    width: 100%;    
    background: #000000;
  }
</style>
