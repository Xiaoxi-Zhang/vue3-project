<script setup>
import { ref } from 'vue';
// vue3中组合式api 组件内部的属性和方法默认是不暴露给父组件的
// 如果想让父组件访问子组件内部的数据，必须通过defineExpose()向外暴露
const msg = ref('this is son msg');
const logMsg = () => {
  console.log(msg.value); 
}
defineExpose({
  msg,
  logMsg
})
</script>

<template>
  <div class="son">
    <h2>子组件</h2>
  </div>
</template>

<style scoped>

.son {
  /* width: 100px; */
  height: 100px;
  border: 1px solid lightblue;
}
</style>