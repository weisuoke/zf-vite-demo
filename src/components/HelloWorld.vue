<template>
  <h1>{{ msg }}</h1>
  <div class="postcss"></div>
  <button @click="handleClick">{{state.count}}</button>
</template>

<script setup lang="ts">
import { reactive, defineProps } from 'vue'
defineProps({
  msg: String
})
interface State {
  count: number;
}
let state = reactive<State>({count: 0});
const handleClick = () => {
  console.log(state.count);
  state.count++
}
</script>

<style scoped>
.postcss {
  height: 50px;
  width: 200px;
  background-color: orange;
  transform: rotate(90deg);
}
</style>
