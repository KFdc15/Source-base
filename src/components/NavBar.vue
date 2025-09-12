<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav class="sticky top-0 z-30 bg-white/80 backdrop-blur border-b border-slate-200">
    <div class="mx-auto max-w-7xl px-4">
      <div class="flex h-16 items-center">
      <!-- Left: Logo -->
        <div class="flex-1 flex items-center gap-2">
          <RouterLink to="/" class="inline-flex items-center gap-2 font-semibold text-slate-800">
            <svg class="h-6 w-6 text-slate-900" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
              <path d="M12 2a10 10 0 1 0 10 10A10.011 10.011 0 0 0 12 2zm1 15h-2v-2h2zm0-4h-2V7h2z"/>
            </svg>
            <span>MyLogo</span>
          </RouterLink>
        </div>

        <!-- Center: Nav links -->
        <div class="hidden md:flex items-center justify-center gap-8">
          <RouterLink to="/" class="text-slate-600 hover:text-slate-900 transition-colors">Home</RouterLink>
          <a href="#" class="text-slate-600 hover:text-slate-900 transition-colors">About</a>
          <a href="#" class="text-slate-600 hover:text-slate-900 transition-colors">Contact</a>
        </div>

        <!-- Right: Auth -->
        <div class="flex-1 flex items-center justify-end gap-3">
          <a href="#" class="px-4 py-2 rounded-md text-slate-700 hover:bg-slate-100 transition-colors">Login</a>
          <a href="#" class="px-4 py-2 rounded-md bg-slate-900 text-white hover:bg-slate-800 transition-colors">Register</a>
        </div>
      </div>
    </div>
  </nav>
</template>