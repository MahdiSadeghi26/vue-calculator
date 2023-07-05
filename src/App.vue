<script setup>
import CalcContainer from './components/CalcContainer.vue'
</script>

<template>
  <div class="container">
  <CalcContainer/>
  </div>
</template>

<style scoped>
.container{
  background-color: var(--light-gray);
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
