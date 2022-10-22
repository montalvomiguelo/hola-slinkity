<script setup lang="ts">
import { ref } from 'vue'
import Note from './Note.vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <h2>{{ msg }}</h2>

  <div>
    <button type="button" @click="count++">count is {{ count }}</button>
    <Note />
  </div>
</template>