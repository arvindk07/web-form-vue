<template>
  <form>
    <label>Email:</label>
    <input type="email" required v-model="email" />
    <label>Password:</label>
    <input type="password" required v-model="password" />
    <label>Role</label>
    <select v-model="role">
      <option value="developer">Web Developer</option>
      <option value="designer">Web Designer</option>
    </select>
  </form>
  <p>EMail: {{ email }}</p>
  <p>Password:{{ password }}</p>
  <p>Role: {{ role }}</p>
</template>

<script>
export default {
  data() {
    return { email: "mario", password: "", role: "" };
  },
};
</script>

<style>
form {
  padding: 40px;
  max-width: 420px;
  margin: 30px auto;
  border-radius: 10px;
  background: #fff;
}
label {
  color: #aaa;
  font-size: 0.75em;
  font-weight: bold;
  margin: 25px 0 15px;
  letter-spacing: 1px;
  display: inline-block;
  text-transform: uppercase;
}
input,
select {
  width: 100%;
  border: none;
  display: block;
  color: #333;
  padding: 10px 6px;
  box-sizing: border-box;
  border-bottom: 1px solid #ddd;
}
</style>
