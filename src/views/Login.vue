<template>
  <section class="login">
    <h1>Login</h1>
    <form>
      <label for="email">Email</label>
      <input type="text" name="email" id="email" v-model="login.email" />
      <label for="senha">Senha</label>
      <input type="password" name="senha" id="senha" />
      <button class="btn" @click.prevent="logar">Logar</button>
    </form>
    <p class="perdeu">
      <a href="/" target="_blank">Esqueceu a Senha?</a>
    </p>
    <LoginCriar />
  </section>
</template>

<script>
import LoginCriar from "@/components/LoginCriar.vue";
export default {
  name: "Login",
  data() {
    return {
      login: {
        email: "",
        psenha: ""
      }
    };
  },
  // methods() {},
  components: {
    LoginCriar
  }
};
</script>

<style scoped>
.login {
  max-width: 500px;
  margin: 0 auto;
  padding: 0 20px;
}
h1 {
  text-align: center;
  font-size: 2rem;
  margin-top: 40px;
  color: #87f;
}
form {
  display: grid;
}
.btn {
  width: 100%;
  max-width: 300px;
  margin: 0 auto;
}
.perdeu {
  text-align: center;
  margin: 20px auto;
}
.perdeu a:hover {
  color: #87f;
  text-decoration: underline;
}
</style>