<script  setup>
import sonCom from "./son-com.vue";

import { reactive, ref, computed, watch, onMounted, onBeforeMount, onUpdated, onBeforeUpdate, onBeforeUnmount, onUnmounted, provide } from 'vue'
// 
// const state =reactive({
//   count:0
// })
const adfasd = ref(1)
provide('aaa', adfasd)
provide('aaa11',()=>{
  adfasd.value++
  console.log(adfasd.value,'---');
  
} )

const list = ref([1, 2, 3, 4, 5, 6])
const computedState111 = computed(() => {
  let aa = list.value.filter(item => item > 3)
  return aa
})
// const state = ref({count:0})
// console.log(state.value.count);
setTimeout(() => {
  list.value.push(9, 10)
}, 3000);
const setCount = () => {
  aaa.value++
  aaa1.value += aaa.value

}
const aaa = ref(0)
const aaa1 = ref('你好')
// console.log(123222);
onMounted(() => {
  console.log('组件挂载完毕onMounted');
})
onBeforeMount(() => {
  console.log('组件挂载前onBeforeMount');
})
onUpdated(() => {
  console.log('修改后onUpdated');

})
onBeforeUpdate(() => {
  console.log('修改前onBeforeUpdate');
})
onBeforeUnmount(() => {
  console.log('页面销毁前onBeforeUnmount');
})
onUnmounted(() => {
  console.log('页面销毁后onUnmounted');
})
// 单个监听
// watch(aaa, (newVal, oldVal) => {
//   console.log(newVal, oldVal);
// })
// 多个监听+立即执行
// watch([aaa,aaa1], ([newaaa, newaaa1],[oldaaa, oldaaa1]) => {
//   console.log(newaaa, newaaa1, oldaaa, oldaaa1);
// }, {immediate: true})
// deep 深度监听
const state1 = ref({ count: 0, age: 12 });
// watch(state1, (newVal, oldVal) => {
//   console.log('变化了');

// },{deep:true})
// 只监听某个具体属性
watch(() => state1.value.count, (newValue, oldValue) => {
  console.log(newValue, oldValue);

})
const setCount1 = () => state1.value.count++
</script>
<template>
  <div>
    <sonCom></sonCom>
    <div>原始 {{ list }}</div>
    <div>非原始 {{ computedState111 }}</div>
    <button @click="setCount1">点击{{ state1.count }}</button>
  </div>
</template>