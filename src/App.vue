<script setup>
import FatherCom from './components/FatherCom.vue';
import { provide, ref } from 'vue';
// 传递普通类型的数据
// let str = '祖先中的数据'
// provide('strKey', str)
// const changeMsg = () => {
//   str = '修改之后的数据'
// }

// 传递响应式数据
// const str = ref('祖先中的数据')
// provide('strKey', str)
// const changeMsg = () => {
//   str.value = '修改之后的数据'
// }

// 让子组件点击按钮的时候，修改祖先组件中的数据
const str = ref('祖先组件中的数据')
provide('strKey', str)
const changeStr = () => {
  str.value = '改变之后的值'
}
// provide不仅可以传递数据，还可以传递方法
provide('changeStr', changeStr)
</script>

<template>
  <div class="box">
    <h1>祖先组件</h1>
    <!-- <button @click="changeMsg">change</button> -->
    <FatherCom></FatherCom>
  </div>
</template>

<style scoped>

.box {
  /* width: 200px; */
  padding: 30px;
  border: 1px solid lightblue;
}
</style>