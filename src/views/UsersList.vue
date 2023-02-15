<template>
  <section class="" id="table">
    <hr />
    <table class="flex">
      <thead>
        <tr class="flex">
          <th>CPF</th>
          <th>Nome</th>
          <th>Detalhes</th>
        </tr>
        <hr />
      </thead>
      <tbody v-for="user in users" :key="user.id" id="conteudo" class="flex">
        <tr>
          <td>{{ user.cpf }}</td>
          <td class="center">{{ user.fullname }}</td>
          <td>
            <button class="">
              <img src="../assets/details-eye.svg" alt="icone detalhe" />
            </button>
          </td>
        </tr>
        <br />
      </tbody>
    </table>
  </section>
</template>

<script>
import axios from "axios";
export default {
  name: "UsersList",

  data() {
    return {
      users: [],
      cpf: "",
    };
  },

  mounted() {
    axios
      .get("http://localhost:8080/api/users")
      .then((response) => {
        this.users = response.data.users;
      })
      .catch((err) => console.log(err));
  },
};
</script>

<style scoped>
table {
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

tr {
  display: inline-flex;
}

tr,
table {
  justify-content: space-between;
}

tbody {
  flex-direction: column;
}

.center {
  margin-right: 2%;
}

td button {
  background-color: transparent;
  border: none;
  cursor: pointer;
}

.hidden {
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
