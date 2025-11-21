<template>
  <div :class="loginStyle">
    Login
  </div>

  <formularioLogin />
</template>

<script>
import formularioLogin from './components/formularioLogin.vue';
export default {
  name: 'App',
  components: {
    formularioLogin,
  },
  data() {
    return {
      loginStyle: 'loginStyle',
    }
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.loginStyle {
  font-family: Avenir, Arial, Helvetica, sans-serif;
  font-size: 20px;
  margin: 20px;
}


</style>
