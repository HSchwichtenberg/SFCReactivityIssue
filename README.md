I a have an issue with a Vue3 Single File Component that behave different in the SFC Playground than in my local Vue CLI Project (fresh project, latest @vue/cli 4.5.15)
In this simple sample the updated of y are printed in the SFC Playground. The updates of y are NOT printed if I copy & paste the code into a Vue CLI project.

I have uploaded the project here: https://github.com/vuejs/vue-next/issues/5248#issuecomment-1011900870

Can anyone explain why SFC Playground and a local Vue CLI Project behave so different?

```
<template>
 <div id="app">
    <div>x should be reactive: x={{x}}
    <div>y should NOT be reactive: y={{y }}</div>
    <button @click="increment">Please click here</button> 
    </div>
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
```
