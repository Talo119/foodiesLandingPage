<template>
  <div id="app" @scroll.capture="getScrollPosition()">
    <!-- Navbar -->
    
    <router-view/>
  </div>
</template>

<script>
import {mapState, mapActions} from 'vuex'
import NavBar from './components/NavBar'
export default {
  components: {
    NavBar,
  },
  data() {
    return {
      scroll_position: '',
    }
  }, 
  created () {
    this.verificarResolucion;
  }, 
  computed: {
    ...mapState(['desktop_mode']),
  },
  methods: {
    getScrollPosition(){
      alert('Entra a funcion');
      this.scroll_position = document.documentElement.scrollTop;
    },

    ...mapActions(['verificarResolucion'])
    
  },
}
</script>

<style>

</style>
