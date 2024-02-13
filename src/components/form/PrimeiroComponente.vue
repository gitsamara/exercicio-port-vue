<template>
  <div class="primeiro-componente-container">
    <h1>Olá, Vue! 👋</h1>
    <p>Meu nome é {{ nome }} e eu sou {{ profissao }}.</p>
    <div class="centralizar"><MultiplosEventos /></div>
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue";

export default {
  name: "PrimeiroComponente",
  components: {
    MultiplosEventos,
  },
  data() {
    return {
      nome: "Samara",
      profissao: "programadora",
    };
  },
};
</script>

<style scoped>
.primeiro-componente-container {
  flex: 1;
  margin-top: 50px;
  text-align: center;
}

.centralizar {
  display: inline-block;
  margin-top: 5px;
}

button {
  padding: 10px;
}
</style>
