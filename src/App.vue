<script setup>
import { ref, onMounted } from 'vue';

// 1. 先生成一个响应式变量
const h1Ref = ref(null);
onMounted(() => {
  console.log(h1Ref.value); 
})
</script>

<template>
  <div class="box">
    <!-- 标签的ref属性的值和响应式对象保持一致 -->
    <h1 ref="h1Ref">这是h1标题</h1>
  </div>
</template>

<style scoped>

.box {
  /* width: 200px; */
  height: 300px;
  border: 1px solid lightcoral;
}
</style>