<template>
  <div class="card border-gray-300 rounded-lg p-4 text-center w-90">
    <img class="w-full h-auto rounded-md" :src="spike.picture" :alt="spike.name" />
    <!-- change size of
    picture -->
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p>Type: {{ props.spike.type }}</p>
    <p>Price: ${{ spike.price }}</p>
    <button @click="addCart()" class="border-2 rounded-[1rem] p-1">Add to Cart</button>
    <!-- remove click for it to work -->
  </div>
</template>

<script setup>
const props = defineProps({
  spike: Object,
})
import { cart } from '@/components/cart'
function addCart() {
  cart.push(props.spike)
  console.log(`${props.spike.name}`)
  console.log(cart)
}
</script>

<style></style>
