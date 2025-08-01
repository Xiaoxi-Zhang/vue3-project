<script setup>
// 使用watch监视响应式数据的变化
// 作用：跟vue2中watch作用一样
import { ref, watch } from 'vue'
const count = ref(0)

watch(count, (newVal, oldVal) => {
  console.log('newVal:', newVal)
  console.log('oldVal:', oldVal)
})
</script>

<template>
  <div>
    <div>count: {{ count }}</div>
    <button @click="count++">count++</button>
  </div>
</template>

<style lang="scss" scoped>

</style>