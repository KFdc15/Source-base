<script setup lang="ts">
import { useCounterStore } from '../stores/counter'
const counter = useCounterStore()
</script>

<template>
  <section class="min-h-[60vh] px-4 py-8">
    <div class="mx-auto max-w-7xl">
      <!-- Heading -->
      <h1 class="text-2xl md:text-3xl font-semibold mb-6">Homepage</h1>

      <!-- Two-card layout -->
      <div class="grid gap-6 md:grid-cols-12">
        <!-- Main large card -->
        <div class="md:col-span-8 lg:col-span-9">
          <div class="card card-compact">
            <h2 class="text-xl font-semibold mb-4">Main Card</h2>
            <p class="mb-4">Count: <span class="font-mono font-bold">{{ counter.count }}</span> (x2 = {{ counter.double }})</p>
            <div class="flex flex-wrap gap-3">
              <button class="px-4 py-2 rounded bg-blue-600 text-white hover:bg-blue-700" @click="counter.inc">Increment</button>
              <button class="px-4 py-2 rounded bg-gray-200 hover:bg-gray-300" @click="counter.reset">Reset</button>
            </div>
          </div>
        </div>

        <!-- Narrow side card -->
        <aside class="md:col-span-4 lg:col-span-3">
          <div class="card">
            <h3 class="text-lg font-semibold mb-3">Side Card</h3>
            <ul class="space-y-2 text-sm text-slate-700">
              <li class="flex items-center justify-between">
                <span>Easy</span>
                <span class="font-medium">0 / 896</span>
              </li>
              <li class="flex items-center justify-between">
                <span>Medium</span>
                <span class="font-medium">0 / 1914</span>
              </li>
              <li class="flex items-center justify-between">
                <span>Hard</span>
                <span class="font-medium">0 / 867</span>
              </li>
            </ul>
          </div>
        </aside>
      </div>
    </div>
  </section>
</template>
