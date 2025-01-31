<template>
  <div>
    <h2 v-for="animal in animals" :key="animal">{{ animal }}</h2>
  </div>
</template>

<script setup>
const animals = ['Zebra', 'Panda', 'Mark', 'Whale']
</script>

<style scoped></style>
