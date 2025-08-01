<script setup>
// 目标：使用deep:true 深度监听对象的变化
import {reactive, ref, watch} from 'vue'

// 使用deep: true 监听整个对象的变化
// const state =ref({count: 0})
// const changeCount = () => {
//   state.value.count++
// }

// watch(state, (newVal, oldVal) => {
//   console.log('newVal:', newVal.count)
//   console.log('oldVal:', oldVal.count)
// }, {
//   deep: true
// })

// reactive生成的响应式对象进行深度监听
const state = reactive({count: 0})
const changeCount = () => {
  state.count++
}
// watch默认可以对reactive生成的响应式对象进行深度监听
watch(state, (newVal, oldVal) => {
  console.log('newVal:', newVal.count)
  console.log('oldVal:', oldVal.count)
})
</script>

<template>
  <div>
    <p>count: {{ state.count }}</p>
    <button @click="changeCount">count++</button>
  </div>
</template>

<style lang="scss" scoped>

</style>    