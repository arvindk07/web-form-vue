<template>
  <form>
    <label>Email:</label>
    <input type="email" required />
  </form>
</template>

<script>
export default {};
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
input {
  width: 100%;
  border: none;
  display: block;
  color: #333;
  padding: 10px 6px;
  box-sizing: border-box;
  border-bottom: 1px solid #ddd;
}
</style>
