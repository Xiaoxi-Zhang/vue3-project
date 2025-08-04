<script setup>
// 1. 子组件的导入
import SonCom from './components/SonCom.vue';

const getMsg = (val) => {
  console.log('接收到子组件传来的消息:', val);
}
</script>

<template>
  <div class="box">
    <h1>父组件</h1>
    <SonCom @send-msg="getMsg"></SonCom>
  </div>
</template>

<style scoped>

.box {
  /* width: 200px; */
  height: 300px;
  border: 1px solid lightcoral;
}
</style>