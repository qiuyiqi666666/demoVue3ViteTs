<script setup>
import { ref, reactive } from 'vue'
let list = ref([{ id: 1, name: 'jack', place: 'phone' }])
const add = () => {
  list.value.push({ id: 1, name: 'jack' + new Date().getTime(), place: 'phone' })
}
const delete1 = (idx) => {
  list.value.splice(idx,1)
}
</script>
<template>
  <div>
    <button @click="add">添加</button>
    <div v-for="(list, idx) in list" :key="idx">
      {{ list.name }}
      <button @click="delete1(idx)">删除</button>
    </div>
  </div>
</template>