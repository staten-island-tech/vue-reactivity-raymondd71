<template>
  <div>
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p class="text-[18px] mt-2">Type: {{ props.spike.type }}</p>
    <p class="text-[18px] mt-2">Price: ${{ spike.price }}</p>
    <button @click="remove($event)" :data-id="spike.id" class="text-[15px] mt-2">Remove</button>
    <!-- Add a button to remove the item -->
  </div>
</template>

<script setup>
const props = defineProps({
  spike: Object,
})
import { cart } from '@/components/cart'
function remove(event) {
  const spikeId = Number(event.target.getAttribute('data-id')) // Get ID from button
  const index = cart.findIndex((item) => item.id === spikeId)

  if (index !== -1) {
    cart.splice(index, 1)
  }
}
</script>

<style scoped></style>
