<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <nav class="fixed top-0 w-full bg-slate-50 h-16 flex items-center gap-4 p-4">
      <RouterLink to="/" class="p-2 border rounded-sm">Home</RouterLink>
      <RouterLink to="/about" class="p-2 border rounded-sm">About</RouterLink>
      <RouterLink to="/test" class="p-2 border rounded-sm">Test</RouterLink>
    </nav>
  </header>
  <RouterView class="pt-16 container mx-auto" />
</template>
