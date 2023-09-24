<template>
    <div>
      <VueWriter :array="externalArray" :eraseSpeed="50" :typeSpeed="100"  />
    </div>
  </template>
  
  <script setup>
  import VueWriter from "vue-writer";
  import { defineProps } from 'vue';
  
  const props = defineProps(['externalArray']);
  </script>
  

  <style>

.is-typed span.cursor {
  display: inline-block;
  width: 3px;
  margin-left: 10px;
  background-color: blue;
  animation: blink 1s infinite;
}

@keyframes blink {
  49% {
    background-color: blue;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}
</style>