<template>
  <button @click.prevent="login">login</button>
</template>

<script>
export default {
  methods: {
    async login() {
      await this.$auth.loginWith("laravelJWT", {
        data: {
          email: "hairulanam21@gmail.com",
          password: "12345"
        }
      });
      this.$router.push("/page2");
    }
  }
};
</script>

<style></style>
