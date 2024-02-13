<template>
  <div>
    <Info :email="email" :esta_trabalhando="false" />
    <Form />
  </div>
</template>

<script>
import Info from "./Info";
import Form from "./Form";

export default {
  name: "Pessoa",
  components: {
    Info,
    Form,
  },
  data() {
    return {
      name: "Samara",
      email: "contato.samarasales@gmail.com",
    };
  },
};
</script>
