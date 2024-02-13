<template>
  <div class="picture-container">
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="mudarImagem" />
  </div>
</template>

<script>
import MudarImagem from "./MudarImagem.vue";

export default {
  name: "Picture",
  components: {
    MudarImagem,
  },
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Samara Sales",
    };
  },
  methods: {
    mudarImagem() {
      this.avatar = "/img/avatarr.png";
    },
  },
};
</script>

<style scoped>
.picture-container {
  flex: 1;
  margin-top: 50px;
  text-align: center;
}
img {
  width: 200px;
  height: auto;
}
</style>
