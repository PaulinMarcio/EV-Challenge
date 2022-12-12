<template>
  <div class="nav-container flex">
    <div class="bar flex">
      <button>CADASTRO</button>
      <button>LISTAGEM</button>
    </div>
    <button class="new">Cadastrar novo usuario</button>
    <div class="table">
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
  </div>
</template>

<script>
export default {
  name: 'Navbar',
}
</script>

<style scoped>
.nav-container{
  flex-direction: column;
  margin-left: 25%;
  margin-top: 5%;
  height: 75vh;
  width: 50vw;
}

.bar{
  width: 100%;
  flex-direction: row;
  justify-content: center;
}

.bar button{
  width: 25%;
  background-color: transparent;
  border: 2px solid transparent;
  padding: 2% 5%;
}
 .bar button, .new, .table button{
  cursor: pointer;
 }
.bar button:active{
  border-bottom: 2px solid black;
}

.flex{
  display: flex;
}

.new{
  border-radius: .3rem;
  border: 0px transparent;
  background-color: #E02B57;
  color: white;
  padding: 0 2%;
  height: 3rem;
  width: 25%;
  margin: 2% 0;
  align-self: flex-end;
}

.table{
  width: 100%;
  height: 100%;
  background-color: white;
}

table{
  flex-direction: column;
}
hr{
  width: 100%;
  color: rgba(0, 0, 0, 0.29);
}

tr, .table table{
  justify-content: space-between;
}

tr{
  padding: 1.5% 0;
}
.center{
  margin-left: -15%;
}
.table button{
  background-color: transparent;
  border: none;
}</style>
