<template>
  <div class="nav-container flex">
    <div class="bar flex">
      <button class="btn" id="bcad">CADASTRO</button>
      <button class="btn sel" id="blist">LISTAGEM</button>
    </div>
    <button class="new" id="new" @click="teste()">Cadastrar novo usuario</button>
    <div class="table" id="table">
      <table class="flex">
        <hr>
        <tr class="flex">
          <th>Nome</th>
          <th>CPF</th>
          <th>Detalhes</th>
        </tr>
        <hr>
        <tr class="flex">
          <td>Márcio Pires Paulin Junior</td>
          <td class="center">111.111.111-11</td>
          <td>
            <button>
              <img src="../assets/details-eye.svg" alt="Mais detalhes">
            </button>
          </td>
        </tr>
        <tr class="flex">
          <td>Márcio Pires Paulin Junior</td>
          <td class="center">111.111.111-11</td>
          <td>
            <button>
              <img src="../assets/details-eye.svg" alt="Mais detalhes">
            </button>
          </td>
        </tr>
        <tr class="flex">
          <td>Márcio Pires Paulin Junior</td>
          <td class="center">111.111.111-11</td>
          <td>
            <button>
              <img src="../assets/details-eye.svg" alt="Mais detalhes">
            </button>
          </td>
        </tr>
        <hr>
      </table>
    </div>
    <div class="hidden" id="cadastro">
      <h3>Insira seus dados:</h3>
      <form>
        <label for="username">Nome:</label><br>
        <input type="text" id="name" name="name"><br>
        <label for="cpf">CPF:</label><br>
        <input type="text" id="cpf" name="cpf"><br>
        <label for="tel">Telefone:</label><br>
        <input type="text" id="tel" name="tel"><br>
        <input type="submit" value="Enviar">
        <input type="reset" value="Limpar">
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Navbar',
  methods: {
    teste() {
      document.getElementById("blist").classList.toggle("sel");
      document.getElementById("bcad").classList.toggle("sel");
      document.getElementById("table").classList.toggle("hidden");
      document.getElementById("cadastro").classList.toggle("hidden");
      var x = document.getElementById("new");
      if (x.innerHTML === "Cadastrar novo usuario"){
        x.innerHTML = "Voltar";
      }
      else{
        x.innerHTML = "Cadastrar novo usuario";
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
  height: 75vh;
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

.sel {
  border-bottom: 2px solid black;
}

.btn {
  width: 25%;
  background-color: transparent;
  padding: 2% 5%;
  border: none
}

.bar button,
.new,
.table button {
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
}

.table {
  width: 100%;
  height: 100%;
  background-color: white;
}

table {
  flex-direction: column;
}

hr {
  width: 100%;
  color: rgba(0, 0, 0, 0.29);
}

tr,
.table table {
  justify-content: space-between;
}

tr,
td {
  padding: 1.5% 0;
}

.center {
  margin-left: -15%;
}

.table button {
  background-color: transparent;
  border: none;
}
</style>
