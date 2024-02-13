<template>
  <div class="container">
    <h2 class="header-title">Fale comigo:</h2>
    <form @submit.prevent="enviarFormulario" class="form-container">
      <div class="form-group">
        <p>Assunto:</p>
        <InputText label="Assunto:" v-model="assunto" class="input-text" />
      </div>
      <div class="form-group">
        <p>Mensagem:</p>
        <InputText label="Mensagem:" v-model="mensagem" class="input-text" />
      </div>
      <div class="form-group">
        <Submit />
      </div>
      <p v-if="enviadoComSucesso" class="success-message">
        Mensagem enviada com sucesso!
      </p>
    </form>
  </div>
</template>

<script>
import InputText from "./InputText.vue";
import Submit from "./Submit.vue";

export default {
  name: "Form",
  components: {
    InputText,
    Submit,
  },
  data() {
    return {
      assunto: "",
      mensagem: "",
      enviadoComSucesso: false,
    };
  },
  methods: {
    enviarFormulario() {
      setTimeout(() => {
        console.log("Formulário enviado!");
        console.log("O assunto é " + this.assunto);
        console.log("A mensagem é " + this.mensagem);

        this.assunto = "";
        this.mensagem = "";

        this.enviadoComSucesso = true;

        setTimeout(() => {
          this.enviadoComSucesso = false;
        }, 2000);
      }, 1000);
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100vh;
}

.header-title {
  align-self: flex-start;
  margin-left: 20px;
}

.form-container {
  width: 200%;
  margin-top: 5px;
}

p {
  margin: 10px 0;
}

.form-group {
  margin-bottom: 20px;
}

.input-text {
  width: 100%;
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 5px;
  box-sizing: border-box;
}

.success-message {
  color: #f23558;
  font-weight: bold;
}
</style>
