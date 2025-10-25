<template>
  <div>
    <div>Register Component</div>

    <div>
      <b>First Name:</b>
      <input type="text" v-model="firstName" />
    </div>

    <div>
      <b>Last Name:</b>
      <input type="text" v-model="lastName" />
    </div>

    <button @click="register">Register</button>

    <div>
      {{ displayName }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Register",
  data() {
    return {
      firstName: "jam",
      lastName: "Estelloso"
    };
  },
  computed: {
    displayName() {
      return `${this.firstName} ${this.lastName}`;
    }
  },
  methods: {
    register() {
      alert(this.displayName);
    },
    goToLogin() {
      alert("go to login page");
    }
  }
};
</script>

<style scoped>
div {
  margin: 8px 0;
}
button {
  margin-top: 10px;
}
</style>
