<template>
  <div>
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p class="text-[18px] mt-2">Type: {{ props.spike.type }}</p>
    <p class="text-[18px] mt-2">Price: ${{ spike.price }}</p>
    <button @click="remove()" class="text-[15px] mt-2">Remove</button>
    <!-- Add a button to remove the item -->
  </div>
</template>

<script setup>
const props = defineProps({
  spike: Object,
})
import { cart } from '@/components/cart'
function remove() {
  cart.splice(props.id, 1)
  console.log(cart)
}
</script>

<style scoped></style>
