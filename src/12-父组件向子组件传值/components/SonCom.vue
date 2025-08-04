<script setup>
// 子组件接受父组件中的数据
// 宏函数（不用导入，直接使用） defineProps
// 直接接受父组件的数据，没加校验
// defineProps(['msg'])
// 如果使用defineProps加类型校验，就得改写成对象的写法
// 如果接受的props的数据想在js逻辑中使用，需要声明一个变量接受defineProps的值
const props = defineProps({
  msg: {
    type: String,
    required: true
  } 
})
console.log(props.msg);

</script>

<template>
  <div class="son">
    <h2>子组件</h2>
    <p>接受的props：{{ msg }}</p>
  </div>
</template>

<style scoped>

.son {
  /* width: 100px; */
  height: 100px;
  border: 1px solid lightblue;
}
</style>