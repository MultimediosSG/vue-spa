<script setup lang="ts">
import { onActivated, onBeforeMount, onBeforeUnmount, onDeactivated, onMounted, onUnmounted, ref } from 'vue';

const counter = ref(0)
onMounted(()=>{

  console.log('onMounted');
  
})
onUnmounted(()=>{

  console.log('onUnmounted');
  
})
onBeforeMount(()=>{

  console.log('onBeforeMount');
  
})
onBeforeUnmount(()=>{

  console.log('onBeforeUnmount');
  
})
onActivated(()=>{

  console.log('onActivated');
  
})
onDeactivated(()=>{

  console.log('onDeactivated');
  
})

</script>

<template>
  <div class="text-center">
    <h1 class="text-4xl font-bold tracking-tighter sm:text-5xl">
      Bienvenido a nuestro sitio web
    </h1>
    <p class="mx-auto max-w-[600px] text-gray-500 md:text-xl">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit.
    </p>
    <p>
      Counter: {{  counter }}
    </p>
    <p>
      <button @click="counter++">++</button>
    </p>
  </div>
</template>
