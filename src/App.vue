<script setup lang="ts">
import { onMounted, ref } from "vue";
// import HelloWorld from "./components/HelloWorld.vue";
// import sonCom from "./components/son-com.vue";
import newDemo from "./components/newDemo.vue";
// const count = ref(100);
// const ref1 = ref(null);
// const comref = ref(null);

// onMounted(() => {
//   console.log(ref1.value); // dom 对象
//   console.log(comref.value); //组件对象

// });
// const sendMSG = (msg) => {
//   // ref 使用
// };
</script>

<template>
  <newDemo></newDemo>
  <!-- <div ref="ref1">
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div> -->
  <!-- <HelloWorld msg="Vite + Vue" /> -->
  <!-- <sonCom
    ref="comref"
    message="我是你爹"
    @sendMSG="sendMSG"
    :count="count"
  ></sonCom> -->
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
