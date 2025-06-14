<script setup lang="ts">
import TheTest from '@/components/TheTest.vue'
import { useCounterStore } from '@/stores/counter'
import { Button } from '@/components/ui/button'
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

const onSubmit = () => {
  console.log(name.value, email.value)
}

const counter = useCounterStore()
</script>

<template>
  <main>
    <TheTest />
    <form @submit.prevent="onSubmit">
      <label for="name">Name</label>
      <input type="text" name="name" id="name" v-model="name" />
      <label for="email">Email</label>
      <input type="email" name="email" id="email" v-model="email" />
      <button @click="clear">Clear</button>
      <button type="submit">Submit</button>
    </form>
    <p>Count: {{ counter.count }}</p>
    <Button @click="counter.increment">IncrementAdd</Button>
  </main>
</template>
