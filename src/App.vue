<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import { Button } from '@/components/ui/button'
import { useCounterStore } from '@/stores/counter'

const counter = useCounterStore()
</script>

<template>
  <header>
    <nav class="fixed top-0 w-full bg-slate-50 h-16 flex items-center gap-4 p-4">
      <Button><RouterLink to="/">Home</RouterLink></Button>
      <Button><RouterLink to="/about">About</RouterLink></Button>
      <Button><RouterLink to="/test">Test</RouterLink></Button>
      <p>Count: {{ counter.count }}</p>
    </nav>
  </header>
  <RouterView class="pt-16 container mx-auto" />
</template>
