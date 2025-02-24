<template>
  <div>
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p class="text-[18px] mt-2">Type: {{ spike.type }}</p>
    <p class="text-[18px] mt-2">Price: ${{ spike.price }}</p>
    <button
      @click="remove(spike.name)"
      class="text-[15px] mt-2 border-1 bg-gray-300 rounded-[1rem] p-1"
    >
      Remove
    </button>
    <!-- Add a button to remove the item -->
  </div>
</template>

<script setup>
const props = defineProps({
  spike: Object,
})
import { cart } from '@/components/cart'

function removeCard(el, index, name) {
  if (el.name === name) {
    cart.splice(index, 1) // takes the position of the card in array and deletes 1 object
  }
}

function remove(name) {
  cart.forEach((el, index) => removeCard(el, index, name)) // takes the name of the card (the whole card in cart)and the position(index) of the card in arary
  // change this so that it only removes the card that the button is pressed from.
}
</script>

<style scoped></style>
