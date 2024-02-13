<template>
  <ul>
    <li><a href="a">Home</a></li>
    <li><a href="a">Projetos</a></li>
    <li v-if="esta_logado">
      <a href="https://www.linkedin.com/in/sa-marasales/">Contato</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "Header",
  props: {
    esta_logado: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  display: flex;
  background: #d93240;
  justify-content: center;
  padding: 0;
  margin: 0;
  border-radius: 6px;
  width: 100%;
}

li {
  margin-right: 50px;
}

a {
  color: white;
  text-decoration: none;
  transition: 0.5s;
  font-size: 18px;
}

a:hover {
  color: #7ff26d;
}
</style>
