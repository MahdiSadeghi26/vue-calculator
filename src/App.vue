<script setup>
import CalcContainer from './components/CalcContainer.vue'
</script>

<template>
  <div class="container">
    <CalcContainer/>
  </div>
</template>

<style scoped lang="scss">
  .container{
    width: 100vw;
    height: 100vh;
    background-color: var(--light-gray);
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
