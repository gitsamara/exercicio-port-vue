<template>
  <div class="app-container">
    <Header :esta_logado="true" />
    <div class="main-content">
      <PrimeiroComponente />
      <Picture />
    </div>
    <p class="paragrafo-pai">{{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
import Header from "./components/form/Header.vue";
import PrimeiroComponente from "./components/form/PrimeiroComponente.vue";
import Picture from "./components/form/Picture.vue";
import LifeCycle from "./components/form/LifeCycle.vue";
import Pessoa from "./components/form/Pessoa.vue";

export default {
  name: "App",
  components: { Header, PrimeiroComponente, Picture, LifeCycle, Pessoa },
  data() {
    return { testando: "" };
  },
};
</script>

<style>
body {
  background-color: #f2c84b;
  color: #0d0d0d;
}

.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.main-content {
  display: flex;
  justify-content: space-between;
  width: 80%;
}

.paragrafo-pai {
  margin: 50px;
}
</style>
