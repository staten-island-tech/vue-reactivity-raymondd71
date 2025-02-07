<template>
  <div class="card border-gray-300 rounded-lg p-4 text-center w-36">
    <img class="w-full h-auto rounded-md" :src="spikes.picture" :alt="spike.name" />
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p>{{ spike.type.join(',') }}</p>
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
