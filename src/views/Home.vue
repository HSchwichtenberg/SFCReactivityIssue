<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Reactivity></Reactivity>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue';
import Reactivity from '@/components/Reactivity.vue'; // @ is an alias to /src

export default defineComponent({
  name: 'Home',
  components: {
    // HelloWorld,
    Reactivity
},
});
</script>
