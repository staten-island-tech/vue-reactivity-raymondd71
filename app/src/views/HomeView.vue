<script setup>
import LogIn from '../components/LogIn.vue'
import AnimalCards from '../components/AnimalCards.vue'
import SpikeCard from '../components/SpikeCard.vue'
import trackSpikes from '@/components/products'
</script>

<template>
  <main>
    <div class="container">
      <SpikeCard v-for="spike in trackSpikes" :spike="spike" :key="spike.name" />
    </div>
    <TheWelcome />
    <AnimalCards class="text-[50px]" />
    <LogIn class="text-red-500" title="Spikes" />
  </main>
</template>
