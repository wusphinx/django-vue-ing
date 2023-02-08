<script>
export default {
  mounted() {
    this.$store.commit("initialiseStore");
  },
  methods: {
    logout() {
      this.$store.commit("logout");
    },
  },
};
</script>

<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>|
    <router-link v-if="!$store.state.email" to="/login">Login</router-link>
    <a v-if="$store.state.email" @click="logout">Logout</a>
  </nav>
  <router-view />
</template>