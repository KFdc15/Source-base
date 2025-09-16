<script setup lang="ts">
import { onMounted, onUnmounted } from 'vue'

const props = defineProps<{ modelValue: boolean }>()
const emit = defineEmits<{ (e: 'update:modelValue', v: boolean): void }>()

const close = () => emit('update:modelValue', false)

const onKey = (e: KeyboardEvent) => {
  if (e.key === 'Escape' && props.modelValue) close()
}

onMounted(() => window.addEventListener('keydown', onKey))
onUnmounted(() => window.removeEventListener('keydown', onKey))
</script>

<template>
  <!-- Backdrop -->
  <transition name="fade">
    <div v-if="modelValue" class="fixed inset-0 z-40 bg-black/40" @click="close" />
  </transition>

  <!-- Drawer -->
  <transition name="slide">
    <aside
      v-if="modelValue"
      class="fixed inset-y-0 left-0 z-50 w-80 max-w-[90vw] bg-white shadow-xl border-r border-slate-200 flex flex-col"
      role="dialog"
      aria-modal="true"
    >
      <div class="flex items-center justify-between h-16 px-4 border-b border-slate-200">
        <div class="inline-flex items-center gap-2">
          <svg class="h-6 w-6 text-slate-900" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path d="M12 2a10 10 0 1 0 10 10A10.011 10.011 0 0 0 12 2zm1 15h-2v-2h2zm0-4h-2V7h2z"/>
          </svg>
          <span class="font-semibold text-slate-800">Menu</span>
        </div>
        <button
          type="button"
          class="p-2 rounded hover:bg-slate-100"
          @click="close"
          aria-label="Close sidebar"
        >
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <nav class="p-4 space-y-1 overflow-y-auto">
        <a href="#" class="block px-3 py-2 rounded hover:bg-slate-100 text-slate-700">Dashboard</a>
        <a href="#" class="block px-3 py-2 rounded hover:bg-slate-100 text-slate-700">Projects</a>
        <a href="#" class="block px-3 py-2 rounded hover:bg-slate-100 text-slate-700">Teams</a>
        <a href="#" class="block px-3 py-2 rounded hover:bg-slate-100 text-slate-700">Settings</a>
      </nav>

      <div class="mt-auto border-t border-slate-200 p-4 text-sm text-slate-500">
        <p>Some extra info can go here.</p>
      </div>
    </aside>
  </transition>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active { transition: opacity 150ms ease; }
.fade-enter-from, .fade-leave-to { opacity: 0; }

.slide-enter-active, .slide-leave-active { transition: transform 200ms ease; }
.slide-enter-from, .slide-leave-to { transform: translateX(-100%); }
</style>
