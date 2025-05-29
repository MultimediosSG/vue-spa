<script setup lang="ts">
import { inject } from 'vue';


const message = inject('message'); // Inyecta el mensaje proporcionado por el layout
const { location, updateLocation } = inject<any>('location');

</script>

<template>
    <button class="bg-red-500 p-2 rounded-2xl" @click="updateLocation">Cambiar ubicación</button>
     <p class="flex-1 text-sm text-gray-500 text-center">
        © 2025 Acme Corporation. Derechos reservados
      </p>
      <p>{{ message }}</p>
      <p>{{ location }}</p>
</template>