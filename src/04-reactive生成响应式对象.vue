<script setup>
// 利用reactive生成响应式数据
// 1. 导入reactive 从vue 按需导入
import { reactive } from 'vue';
// 注意：reactive只能声明响应的对象。简单类型的响应数据不能使用reactive。简单类型的响应式数据使用ref
const state = reactive({count: 0})
const changeCount = () => {
  state.count++;
}
</script>

<template>
  <div>count:{{ state.count }}</div>
  <button @click="changeCount">count++</button>
</template>

<style lang="scss" scoped>

</style>