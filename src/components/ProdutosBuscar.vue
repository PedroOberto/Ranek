<template>
  <form>
    <input type="text" id="busca" name="busca" v-model="busca" placeholder="Buscar..." />
    <input type="submit" id="lupa" name="lupa" value="Buscar" @click.prevent="buscarProdutos" />
  </form>
</template>

<script>
export default {
  data() {
    return {
      busca: ""
    };
  },
  methods: {
    buscarProdutos() {
      this.$router.push({ query: { q: this.busca } });
    }
  }
};
</script>

<style scoped>
form {
  max-width: 600px;
  margin: 30px auto 60px;
  position: relative;
}
#busca {
  width: 100%;
  padding: 20px;
}
#lupa {
  width: 62px;
  height: 62px;
  background: url("../assets/search.svg") no-repeat center center;
  border: none;
  text-indent: -150px;
  cursor: pointer;
  position: absolute;
  top: 0px;
  right: 0px;
  box-shadow: none;
}
</style>