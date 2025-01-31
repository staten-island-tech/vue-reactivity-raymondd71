<script setup>
import LogIn from '../components/LogIn.vue'
import AnimalCards from '../components/AnimalCards.vue'
</script>

<template>
  <main>
    <TheWelcome />
    <AnimalCards class="text-blue-500" />
    <LogIn class="text-red-500" message="I hate black berries" />
  </main>
</template>
