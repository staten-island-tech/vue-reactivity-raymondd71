<template>
  <div>
    <h2 class="text-lg font-semibold mt-2">{{ spike.name }}</h2>
    <p class="text-[18px] mt-2">Type: {{ props.spike.type }}</p>
    <p class="text-[18px] mt-2">Price: ${{ spike.price }}</p>
    <button class="text-[15px] mt-2">Remove</button>
    <!-- Add a button to remove the item -->
  </div>
</template>

<script setup>
const props = defineProps({
  spike: Object,
})
</script>

<style scoped></style>
