<template>

  <div class="container-fluid">
    <NavBar class="minavbar d-block d-sm-none"/>
    <NavBar class="d-none d-sm-block"/>
    <!-- INICIO -->
    <section id="home" class="home">   
      <HomePage/>      
    </section>
    <!-- ACERCA DE -->
    <section id="acercade" :class="desktop_mode ? 'acercade' : 'acercade-sm'">      
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
    <section id="beneficios" :class="desktop_mode ? 'befenicios' : 'befenicios-sm'">
      <Beneficios/>
    </section>
    <!-- FOOTER -->
    <section id="footer">
      <Footer/>
    </section>
  </div>
  
</template>

<script>
// @ is an alias to /src
import {mapState, mapActions} from 'vuex'
import NavBar from '../components/NavBar'
import HomePage from '../components/HomePage'
import AcercaDe from '../components/AcercaDe'
import Sucursales from '../components/Sucursales'
import Testimonios from '../components/Testimonios'
import Contactanos from '../components/Contactanos'
import Beneficios from '../components/Beneficios'
import Footer from '../components/Footer'


export default {
  name: 'Home',
  components: {
    NavBar,HomePage, AcercaDe,Sucursales, Testimonios,Contactanos, Beneficios,Footer
  },
  data() {
    return {
      
    }
  },
  created () {
    this.verificarResolucion();
  },
  computed: {
    ...mapState(['desktop_mode'])

  },
  methods: {    
    ...mapActions(['verificarResolucion'])
  },
}
</script>
<style>
  .acercade{
    height: 650px;    
  }
  .acercade-sm{
    height: 1000px;    
  }
  .testimonios{
    height: 650px;
  }
  .contactanos{
    position: absolute;
    width: 100%;    
    background: #000000;
  }
  .beneficios{
    height: 500px;
  }
  .beneficios-sm{
    height: 1100px;
  }
  .footer{
    top: 1500px;
  }
  .minavbar{
    width: 360px;
  }
</style>
