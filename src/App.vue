<script setup>
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
