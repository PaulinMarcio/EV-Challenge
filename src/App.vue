<template>
  <div id="app">
    <Header></Header>
    <Navbar></Navbar>
    <div class="view-container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Navbar from "./components/Navbar.vue"

export default {
  name: 'App',
  data() {
    return {
      headerTitle: "Usuarios"
    }
  },
  components: {
    Header,
    Navbar
  }
}
</script>

<style>
/* SINTA-SE A VONTADE PARA ALTERAR ESSAS ESTILIZA��ES BASICAS */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Roboto', sans-serif;
}

.view-container{
  margin-left: 25%;
  width: 50vw;
}
</style>
