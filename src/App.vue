<template>
<div id="app">

  <Header/>
  <Home />

  <h1>teste</h1>

</div>
</template>

<script>
import "./style/global.css";
import Header from "./components/Header.vue";
import Home from "./pages/home.vue"

export default {
  name: 'App',
  components: {
    Header,
    Home
    
  }
}
</script>


<style>

</style>
