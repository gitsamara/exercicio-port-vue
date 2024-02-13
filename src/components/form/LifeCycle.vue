<template>
  <h1>{{ name }}</h1>
</template>

<script>
import Info from "./Info.vue";

export default {
  name: "LifeCycle",
  data() {
    return {
      name: "Seja",
    };
  },
  created() {
    setTimeout(() => {
      this.name = "bem-vindo!";
    }, 1000);

    this.lifeCycle();
  },
  mounted() {
    setTimeout(() => {
      this.name = "Seja bem-vindo! ;)";
    }, 2000);

    this.lifeCycle();
  },
  methods: {
    lifeCycle() {
      console.log("Executou");
    },
  },
};
</script>
