<template>
  <div>
    <p class="status-message" v-if="esta_trabalhando">
      Estou trabalhando no momento.
    </p>
    <p class="status-message" v-else>Estou em busca de novas oportunidades.</p>
    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
      <li
        v-for="(technology, index) in backend_technologies"
        v-bind:key="index"
      >
        {{ technology }}
      </li>
    </ul>
    <p>E para front-end utilizo as seguintes linguagens:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
    <p class="paragrafo-pai">
      Para acessar meu portfólio,
      <a v-bind:href="meu_link" target="_blank">clique aqui</a>.
    </p>
    <div class="button-container">
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p class="mostrar-email" v-show="mostrar_email">
      <strong>{{ email }}</strong>
    </p>
  </div>
</template>

<script>
export default {
  name: "Info",
  components: {},
  props: {
    email: String,
    esta_trabalhando: Boolean,
  },
  data() {
    return {
      mostrar_email: false,
      meu_link: "https://github.com/gitsamara",
      textoBotao: "Mostrar e-mail",
      backend_technologies: ["C", "Python", "Java", "JavaScript"],
      frontend_technologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "Vue" },
      ],
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textoBotao = "Mostrar E-mail";
      } else {
        this.textoBotao = "Esconder E-mail";
      }
    },
  },
};
</script>

<style>
.paragrafo-pai {
  color: #0d0d0d;
}

.status-message {
  text-align: center;
}

.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 10px;
}

.mostrar-email {
  text-align: center;
  font-weight: bold;
}
</style>
