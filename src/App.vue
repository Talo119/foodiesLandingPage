<template>
  <div id="app" @scroll.capture="getScrollPosition()">
    <!-- Navbar -->
    <NavBar/>
    <router-view/>
  </div>
</template>

<script>
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
  methods: {
    getScrollPosition(){
      alert('Entra a funcion');
      this.scroll_position = document.documentElement.scrollTop;
    },
    
  },
}
</script>

<style>

</style>
