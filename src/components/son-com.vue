<script setup>
// 父传子
import { onMounted, ref,inject } from "vue";
const aa =inject('aaa')
const aaa11 =inject('aaa11')


console.log(aa.value,'=11122=');

const props = defineProps({
  message: String,
  count: Number
})
setTimeout(() => {
  console.log(props.count);

}, 1000)
const aaaa = ref(123)

// 子传父
const emit = defineEmits(['sendMSG'])
const sendMsg = ()=>{
  console.log('发送',aaaa.value);
// emit('sendMSG', '发送')

  
}
defineExpose({ //defineExpose 把组件内部属性暴露出去
  aaaa,
  sendMsg
})
</script>
<template>
  <div>{{ message }}{{ count }}</div>
  <button @click="aaa11">发送{{ aa.value }}</button>
</template>