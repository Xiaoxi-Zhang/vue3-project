<script setup>
// 1.导入对应的生命周期钩子
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated } from 'vue'
console.log('setup: 组件正在加载');

onBeforeMount(() => {
  console.log('onBeforeMount: 组件即将挂载');
})
onMounted(() => {
  console.log('onMounted1: 组件1已挂载');  
})
onBeforeUpdate(() => {
  console.log('onBeforeUpdate: 组件即将更新');
})
onUpdated(() => {
  console.log('onUpdated: 组件已更新');
})

// 变化：生命周期钩子可以多次调用
onMounted(() => {
  console.log('onMounted2: 组件2已挂载');
})
const count = ref(0)
</script>

<template>
  <div>
    <p>count:{{ count }}</p>
    <button @click="count++">count++</button>
  </div>
</template>

<style lang="scss" scoped>

</style>