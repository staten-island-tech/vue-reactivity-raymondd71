<script setup>
import LogIn from '../components/LogIn.vue'
import AnimalCards from '../components/AnimalCards.vue'
</script>

<template>
  <main>
    <TheWelcome />
    <AnimalCards class="text-[50px]" />
    <LogIn class="text-red-500" title="Spikes" />
  </main>
</template>
