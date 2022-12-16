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

        <span>
          <label for="cpf">CPF:</label>
          <input type="text" id="cpf" name="cpf"><br>
        </span>

        <span>
          <input class="new" type="submit" value="Enviar">
          <input class="new" type="reset" value="Limpar">
        </span>

        <hr>
      </form>
    </section>
</template>

<script>
export default {
  name: 'Register',
}
</script>

<style scoped>
.hidden {
  display: none;
}
.new{
  cursor: pointer;
  border-radius: .3rem;
  border: 0px transparent;
  background-color: #E02B57;
  color: white;
  padding: 0 2%;
  min-height: 3rem;
  width: 25%;
  margin: 2% 0;
}
.new:active {
  background-color: #b82248;
}

hr {
  width: 100%;
  color: rgba(0, 0, 0, 0.29);
}

form{
  display: grid;
  column-count: 5;
  row-gap: 10%;
}
</style>