<script setup>
// 目标：computed的使用
// 作用：跟vue2中的computed一模一样
// 1.导入
import {ref, computed} from 'vue'
const count = ref(0)

const doubleCount = computed(() => {
  return count.value * 2
})
</script>

<template>
  <div>
    <div>doubleCount: {{ doubleCount }}</div>
    <button @click="count++">count++</button>
  </div>
</template>

<style lang="scss" scoped>

</style>