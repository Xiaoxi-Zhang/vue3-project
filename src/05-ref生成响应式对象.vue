<script setup>
// 目标：利用ref把简单类型的数据生成响应式对象
// 1.导入ref
import { ref } from 'vue'

// const count = ref(0)
// const changeCount = () => {
//   // 在script 使用ref生成的响应式对象。如果想访问这个对象的原始值，必须加 .value
//   // 但是，在模板中使用响应对象不用加.value
//   // console.log(count.value);
//   count.value++
  
//   // count.value++
// }

const state = ref({count: 0})
const changeCount = () => {
  state.value.count++
}

</script>

<template>
  <div>count:{{ state.count }}</div>
  <button @click="changeCount">count++</button>
</template>

<style lang="scss" scoped>

</style>