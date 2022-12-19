<template>
  <section class="" id="cadastro">

    <form>
      <hr>
      <h3>Insira seus dados:</h3>
      <hr>
      <span>
        <label for="username">Nome:</label>
        <input type="text" id="name" name="name"><br>
      </span>
      <br>

      <span>
        <label for="cpf">CPF:</label>
        <input v-model="cpfuser" v-mask="'###.###.###-##'" type="text" id="cpf" name="cpf"><br>
      </span>
      <br>

      <span class="right">
        <input class="new" type="submit" value="Enviar">
        <input class="new" type="reset" value="Limpar">
      </span>
      <br>

      <hr>
    </form>
  </section>
</template>

<script>
export default {
  name: 'Register',
  methods: {
    data(){
      return{
        user:[],
        cpfuser:"",
        username:"",
      }
    }
  }
}
</script>

<style scoped>
.new {
  cursor: pointer;
  border-radius: .3rem;
  border: 0px transparent;
  background-color: #E02B57;
  color: white;
  padding: 0 2%;
  min-height: 3rem;
  min-width: 10rem;
  margin: 2% 0;
}

.new:active {
  background-color: #b82248;
}

hr {
  width: 100%;
  color: rgba(0, 0, 0, 0.29);
}

form {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  height: 40vh;
}
</style>