<!-- Vue.js Template -->
<template>
 <div id="app">
   <div>x should be reactive: x={{x}}</div>
    <div>y should NOT be reactive: y={{y }}</div>
    <button @click="increment">Please click here</button> 
  </div>
</template>

<script setup lang="ts">
import {  ref } from 'vue';

let x = ref(0);
let y = 0; // no RefImpl

function increment()
{
    x.value++; 
    y++; 
}
</script>