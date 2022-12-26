<template>
  <section class="" id="cadastro">
    <form>
      <hr />
      <h3>Insira seus dados:</h3>
      <hr />
      <span>
        <label for="name">Nome:</label>
        <input v-model="name" type="text" id="name" name="name" />
        <br />
      </span>
      <br />

      <span>
        <label for="cpf">CPF:</label>
        <input
          v-model="cpf"
          v-mask="'###.###.###-##'"
          type="text"
          id="cpf"
          name="cpf"
        /><br />
      </span>
      <br />

      <span class="right">
        <input class="new" type="submit" value="Enviar" @click="postUser" />
        <input class="new" type="reset" value="Limpar" />
      </span>
      <br />

      <hr />
    </form>
  </section>
</template>

<script>
import axios from 'axios'
export default {
  name: "Register",

  methods: {

    postUser() {
      axios
        .post("/api/users", { fullname: this.name, cpf: this.cpf })
        .then(() => {
          console.log("Usuário cadastrado com sucesso");
        })
        .catch((error) => {
          console.log(error);
        });
      this.$root.$refs.A.change();
    },
  },

  data() {
    return {
      dataUsers: [],
      cpf: "",
      name: "",
    };
  },
};
</script>

<style scoped>
.new {
  cursor: pointer;
  border-radius: 0.3rem;
  border: 0px transparent;
  background-color: #e02b57;
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
