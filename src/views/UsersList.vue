<template>
  <section class="" id="table">
    <hr>
    <table class="flex">

      <tr class="flex">
        <th>CPF</th>
        <th>Nome</th>
        <th>Detalhes</th>
      </tr>
      <hr>
      <tr class="flex">
        <td>111.111.111-11</td>
        <td class="center">Márcio Pires Paulin Junior</td>
        <td>
          <button>
            <img src="../assets/details-eye.svg" alt="Mais detalhes">
          </button>
        </td>
      </tr>
      <tr class="flex">
        <td>111.111.111-11</td>
        <td class="center">Márcio Pires Paulin Junior</td>
        <td>
          <button>
            <img src="../assets/details-eye.svg" alt="Mais detalhes">
          </button>
        </td>
      </tr>
      <tr class="flex">
        <td>111.111.111-11</td>
        <td class="center">Márcio Pires Paulin Junior</td>
        <td>
          <button>
            <img src="../assets/details-eye.svg" alt="Mais detalhes">
          </button>
        </td>
      </tr>
      <hr>
    </table>
  </section>
</template>

<script>
import axios from 'axios'
export default {
  name: 'UsersList'
}
</script>

<style scoped>
table {
  display: flex;
  height: 100%;
  background-color: white;
  flex-direction: column;
}

section {
  width: 50vw;
}

hr {
  width: 100%;
  color: rgba(0, 0, 0, 0.29);
}

tr,
table {
  justify-content: space-between;
}

.center {
  margin-left: 3.5%;
}

table button {
  background-color: transparent;
  border: none;
  cursor: pointer;
}
.hidden{
  display: none;
}
.flex {
  display: flex;
}

tr,
td {
  padding: 1.5% 0;
}
</style>