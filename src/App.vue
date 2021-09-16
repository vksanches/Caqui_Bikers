<template>
<div id="app">

  <Header/>
  <Home />
  <Footer />


</div>
</template>

<script>
import "./style/global.css";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Home from "./pages/home.vue"

export default {
  name: 'App',
  
  components: {
    Header,
    Home,
    Footer
    
  }
}
</script>


<style>

</style>
