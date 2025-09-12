<template>
  <!-- Sidebar component controlled internally -->
  <Sidebar v-model="open" />

  <!-- Floating hamburger button -->
  <button
    v-if="!open"
    @click="open = true"
    aria-label="Open menu"
    class="fixed bottom-6 left-6 z-40 h-12 w-12 rounded-full bg-slate-900 text-white shadow-lg flex items-center justify-center hover:bg-slate-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-slate-400"
  >
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.8" stroke="currentColor" class="w-6 h-6">
      <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
    </svg>
  </button>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Sidebar from './Sidebar.vue'

const open = ref(false)
</script>
