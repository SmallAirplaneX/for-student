<script setup>
import { onMounted, ref } from 'vue';
const newData = ref({
  price: "10"
})

const data = ref({})
const input = ref('')
onMounted(() => {
   setTimeout(() => {
    Object.assign(data.value, newData.value)
  },3000)
})
console.log(data.value)
console.log(newData.value)
console.log(data.value.price)
</script>

<template>
{{ data }}
<br />
{{ data.price }}
<div class="test">
  <p>red</p>
  <el-input v-model="input" style="width: 240px" placeholder="Please input" />
</div>
</template>

<style scoped>
::v-deep(.el-input) {
  .el-input__wrapper {
    box-shadow:0 0 0 0 
  }
}


</style>
