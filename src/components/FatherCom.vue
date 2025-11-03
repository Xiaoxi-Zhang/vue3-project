<script setup>
import SonCom from './SonCom.vue';
</script>

<template>
  <div class="father">
    <h2>父组件</h2>
    <SonCom></SonCom>
  </div>
</template>

<style scoped>

.father {
  padding: 30px;
  border: 1px solid lightgreen;
}
</style>