<script setup lang="ts">
import { inject } from 'vue';
import FooterCopyright from './FooterCopyright.vue';
const message = inject('message');
</script>

<template>
    <footer class="flex items-center h-14 px-4 border-t border-gray-300 sm:h-16 md:px-6 lg:px-8">
        {{ message }}
     <FooterCopyright />
    </footer>
</template>