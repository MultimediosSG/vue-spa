<script setup lang="ts">
import ButtonSite from '@/components/ButtonSite.vue';
import { onActivated, onBeforeMount, onBeforeUnmount, onDeactivated, onMounted, onUnmounted, ref } from 'vue';

const counter = ref(0)
onMounted(() => {

  console.log('onMounted');

})
onUnmounted(() => {

  console.log('onUnmounted');

})
onBeforeMount(() => {

  console.log('onBeforeMount');

})
onBeforeUnmount(() => {

  console.log('onBeforeUnmount');

})
onActivated(() => {

  console.log('onActivated');

})
onDeactivated(() => {

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
      Counter: {{ counter }}
    </p>
    <p class="flex gap-2">
      <!-- <button @click="counter++">++</button> -->
      <ButtonSite class="flex gap-2">
        sumar un digito
        <template v-slot:icono>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 13.5 12 21m0 0-7.5-7.5M12 21V3" />
          </svg>
        </template>
      </ButtonSite>
      <ButtonSite>
        ++
      </ButtonSite>
      <ButtonSite class="flex gap-2" @click="counter++">
        ++ Sumar
        <template v-slot:icono>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 6h9.75M10.5 6a1.5 1.5 0 1 1-3 0m3 0a1.5 1.5 0 1 0-3 0M3.75 6H7.5m3 12h9.75m-9.75 0a1.5 1.5 0 0 1-3 0m3 0a1.5 1.5 0 0 0-3 0m-3.75 0H7.5m9-6h3.75m-3.75 0a1.5 1.5 0 0 1-3 0m3 0a1.5 1.5 0 0 0-3 0m-9.75 0h9.75" />
          </svg>

        </template>
      </ButtonSite>
    </p>
  </div>
</template>
