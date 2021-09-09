<template>
  <HelloWorld msg="Vue3 + Vite" />
  <div class="avatar"></div>
</template>

<script setup>
import HelloWorld from "./components/HelloWorld.vue";
fetch("/api/todos/1")
  .then((response) => response.json())
  .then((json) => console.log(json));
</script>

<style scoped>
.avatar {
  width: 200px;
  height: 200px;
  background-image: url(@/assets/avatar.png);
  background-size: contain;
}
</style>
