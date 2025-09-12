<script setup lang="ts">
import NavBar from './components/NavBar.vue';
import SidebarToggle from './components/SidebarToggle.vue'
import AppFooter from './components/AppFooter.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <NavBar />
  <SidebarToggle />
  <RouterView />
  <AppFooter />
</template>

