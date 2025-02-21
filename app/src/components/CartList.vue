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
  const index = cart.findIndex((key) => key.name === this.props.spike.id)
  cart.splice(props.spike.index, 1) // change this so that it only removes the card that the button is pressed from.-

  /*const target = update.cart.findIndex((key) => key.name === this.product.name);

  update.cart.splice(target, 1); */
}
</script>

<style scoped></style>
