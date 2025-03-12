<script setup>
// import Mobile from "./components/mobile.vue";
// import Intro from "./components/intro.vue";
// import Home from "./components/home.vue";

import { ref, onMounted } from "vue";

const showintro = ref(true);

onMounted(() => {
  setTimeout(() => {
    showintro.value = false;
  }, 6000);
  return {
    showintro,
  };
});
</script>

<template>
  <router-view></router-view>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
