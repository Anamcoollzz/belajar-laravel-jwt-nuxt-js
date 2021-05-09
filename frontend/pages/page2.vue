<template>
  <div>
    <h1>Saya sudah login {{ $auth.user.name }}</h1>
    <button @click.prevent="logout">logout</button>
    kenapa
  </div>
</template>

<script>
export default {
  middleware: "auth",

  methods: {
    logout() {
      this.$auth.logout();
    }
  },

  mounted() {
    // console.log(this.$auth.user);
  }
};
</script>

<style></style>
