<script setup>
const msg = 'this is a message'
    const logMsg = () => {
      console.log(msg)
    }
</script>

<template>
  <div>
    <div>msg: {{ msg }}</div>
    <button @click="logMsg">打印msg</button>
  </div>
</template>

<style lang="scss" scoped>

</style>