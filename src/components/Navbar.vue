<template>
  <div class="nav-container flex">
    <div class="bar flex">
      <p class="" id="bcad">CADASTRO</p>
      <p class="sel" id="blist">LISTAGEM</p>
    </div>
    <button class="new" id="new" @click="change()">Cadastrar novo usuario</button>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  created() {
        this.$root.$refs.A = this;
    },
  methods: {

    change() {
      document.getElementById("blist").classList.toggle("sel");
      document.getElementById("bcad").classList.toggle("sel");
      
      var x = document.getElementById("new");


      if (x.innerHTML === "Cadastrar novo usuario"){
        x.innerHTML = "Voltar";
        this.$router.push('/register');
      }
      else{
        x.innerHTML = "Cadastrar novo usuario";
        this.$router.push('/');
      }
    }
  }
}
</script>

<style scoped>
.nav-container {
  flex-direction: column;
  margin-left: 25%;
  margin-top: 5%;
  width: 50vw;
}

.bar {
  width: 100%;
  flex-direction: row;
  justify-content: center;
}

.hidden {
  display: none;
}

.sel
{
  color: black !important;
  border-bottom: 2px solid black !important;
}

.bar p {
  width: 25%;
  color: gray;
  background-color: transparent;
  padding: 2% 5%;
  border: none;
  text-align: center;
}

.bar button,
.new{
  cursor: pointer;
}

.flex {
  display: flex;
}

.new {
  border-radius: .3rem;
  border: 0px transparent;
  background-color: #E02B57;
  color: white;
  padding: 0 2%;
  min-height: 3rem;
  width: 25%;
  margin: 2% 0;
  align-self: flex-end;
}

.new:active {
  background-color: #b82248;
}</style>
