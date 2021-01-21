<template>

  <div class="container-fluid">
    <section id="home" class="home">   
      <HomePage/>      
    </section>
    <section id="acercade" class="acercade">      
      <AcercaDe/>      
    </section>
    <section id="sucursales" class="mx-0 px-0">
      <Sucursales/>
    </section>

  </div>
  
</template>

<script>
// @ is an alias to /src
import HomePage from '../components/HomePage'
import AcercaDe from '../components/AcercaDe'
import Sucursales from '../components/Sucursales'


export default {
  name: 'Home',
  components: {
    HomePage, AcercaDe,Sucursales
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
</style>
