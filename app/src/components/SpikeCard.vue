<template>
  <div class="card border-gray-300 rounded-lg p-4 text-center w-90">
    <img class="w-full h-auto rounded-md" :src="spike.picture" :alt="spike.name" />
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p>Type: {{ props.spike.type }}</p>
    <p>Price: ${{ spike.price }}</p>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'
const props = defineProps({
  spike: {
    type: Object,
    required: true,
  },
})
</script>

<style></style>
