<script setup lang="ts">
import TheTest from '../components/TheTest.vue'

import { ref, onMounted } from 'vue'

const name = ref('')
const email = ref('')

const clear = () => {
  name.value = ''
  email.value = ''
}

onMounted(() => {
  console.log('mounted')
})
</script>

<template>
  <main>
    <TheTest />
    <input v-model="name" placeholder="Type something..." />
    <p>You typed: {{ name }}</p>
    <input v-model="email" placeholder="Type something..." />
    <p>You typed: {{ email }}</p>
    <button @click="clear">Clear</button>
  </main>
</template>
