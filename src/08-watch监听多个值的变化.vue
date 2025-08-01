<script setup>
// 使用watch监视多个响应式数据的变化
// 作用：跟vue2中watch作用一样
import { ref, watch } from 'vue'
const count = ref(0)
const age = ref(18)

// watch(count, (newVal, oldVal) => {
//   console.log('newVal:', newVal)
//   console.log('oldVal:', oldVal)
// })
// watch(age, (newAge, oldAge) => {
//   console.log('newAge:', newAge)
//   console.log('oldAge:', oldAge)
// })

// 使用watch同时监听两个值的变化
watch([count, age], (newVal, oldVal) => {
  // newVal和oldVal也变成了一个数组
  // 数组中值的顺序和watch监听的响应式数据的顺序一致
  // newVal是新值, oldVal是老值
  console.log('newVal:', newVal)
  console.log('oldVal:', oldVal)
})
</script>

<template>
  <div>
    <div>count: {{ count }}</div>
    <button @click="count++">count++</button>
    <div>age: {{ age }}</div>
    <button @click="age++">age++</button>
  </div>
</template>

<style lang="scss" scoped>

</style>