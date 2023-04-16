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
    <label>Skills:</label>
    <input type="text" v-model="tempSkill" @keyup.alt="addskill" />
    <div v-for="skill in skills" :key="skill" class="pill">
      <span @click="deleteSkill(skill)">{{ skill }}</span>
    </div>
    <div class="terms">
      <input type="checkbox" required v-model="terms" />
      <label>AccepttTerms and conditions</label>
    </div>
  </form>
  <p>EMail: {{ email }}</p>
  <p>Password:{{ password }}</p>
  <p>Role: {{ role }}</p>
  <p>Terms accepted: {{ terms }}</p>
</template>

<script>
export default {
  data() {
    return {
      email: "mario",
      password: "",
      role: "designer",
      terms: "true",
      tempSkill: "",
      skills: [],
    };
  },
  methods: {
    addskill(e) {
      if (e.key === "," && this.tempSkill) {
        if (!this.skills.includes(this.tempSkill)) {
          this.skills.push(this.tempSkill);
        }
        this.tempSkill = "";
      }
    },

    deleteSkill(skill) {
      this.skills = this.skills.filter((item) => {
        return skill !== item;
      });
    },
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

input[type="checkbox"] {
  top: 2px;
  width: 16px;
  margin: 0 10px 0 0;
  position: relative;
  display: inline-block;
}
.pill {
  font-size: 12px;
  color: #777;
  cursor: pointer;
  font-weight: bold;
  border-radius: 20px;
  letter-spacing: 1px;
  background: #eee;
  padding: 6px 12px;
  margin: 20px 10px 0 0;
  display: inline-block;
}
</style>
