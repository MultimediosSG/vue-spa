<script setup lang="ts">
import FooterSite from '@/components/FooterSite.vue';
import { provide, ref } from 'vue';

provide('message', 'hola!');
const location = ref('Liberia')

function updateLocation() {
  location.value = 'San José';
}

provide('location', {
  location,
  updateLocation
})

</script>

<template>
  <div class="flex flex-col h-screen">
    <!-- Header -->
    <header class="flex items-center h-14 px-4 border-b border-gray-300 sm:h-16 md:px-6 lg:px-8">
      <div>
        <a class="flex items-center gap-2 font-semibold" href="#">
          <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="40" height="40" />
        </a>
          {{ location }}
      </div>
      <nav class="ml-auto space-x-4 flex items-center h-10 sm:space-x-6">
        <RouterLink to="/"> Home </RouterLink>
        <RouterLink :to="{ name: 'features' }"> Features </RouterLink>
        <RouterLink to="/pricing"> Pricing </RouterLink>
        <RouterLink to="/about"> About (protegida) </RouterLink>
        <RouterLink to="/contact"> Contact </RouterLink>
      </nav>
    
    </header>
    <!-- Fin Header -->

    <!-- Main -->
    <main class="flex-1 flex items-center justify-center">
      <!-- <RouterView /> -->
      <router-view v-slot="{ Component }">
        <keep-alive>
          <component :is="Component" />
        </keep-alive>
      </router-view>
    </main>
    <!-- Fin Main -->

    <!-- Footer -->
    <FooterSite />
    <!-- Fin Footer -->
  </div>
</template>