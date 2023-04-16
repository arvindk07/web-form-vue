<template>
  <SignupForm />
</template>

<script>
import SignupForm from "./components/SignupForm.vue";
export default {
  name: "App",
  components: {
    SignupForm,
  },
};
</script>

<style>
#app {
  margin-top: 60px;
  color: #2c3e50;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
body {
  background: rgb(236, 233, 233);
}
</style>
