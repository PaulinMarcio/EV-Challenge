<template>
  <header>
    <button>
      <img src="../assets/close.svg" alt="">
    </button>
    <h1>CADASTRO DE USUARIO</h1>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
header{
  background-color: #E02B57;
  display: flex;
  height: 2rem;
  align-items: center;
  justify-content: center;
  color: white;
}

button{
  position: absolute;
  left: 1rem;
  background-color: transparent;
  border: none;
  cursor: pointer;
}

h1{
  font-size: .8rem;
}

</style>
