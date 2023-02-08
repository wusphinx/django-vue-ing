<script setup>
import { ref } from "vue";

const user = ref("input name");
const password = ref("input password");

function login() {
  // TODO: check password
}
</script>

<template>
  <h2>从0到1</h2>
  <p><input v-model="user" /> {{ text }}</p>
  <p><input v-model="password" /> {{ text }}</p>

  <button @click="login">登录</button>
</template>