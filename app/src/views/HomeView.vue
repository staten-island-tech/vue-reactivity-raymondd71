<script setup>
import LogIn from '../components/LogIn.vue'
import AnimalCards from '../components/AnimalCards.vue'
import trackSpikes from '../components/products.js'
</script>

<template>
  <main>
    <TheWelcome />
    <AnimalCards class="text-[50px]" />
    <LogIn class="text-red-500" title="Spikes" />
    <trackSpikes />
  </main>
</template>
