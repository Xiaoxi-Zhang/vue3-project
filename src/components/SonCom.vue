<script setup>
import { inject } from 'vue';
const str = inject('strKey'); // 获取祖先组件传递的数据
const changeStr = inject('changeStr')
const handleClick = () => {
  changeStr()
}
</script>

<template>
  <div class="son">
    <h3>孙子组件</h3>
    <p>接受祖先组件的数据: {{ str }}</p>
    <button @click="handleClick">改变str的数据</button>
  </div>
</template>

<style scoped>

.son {
  /* width: 100px; */
  padding: 30px;
  border: 1px solid lightsalmon;
}
</style>