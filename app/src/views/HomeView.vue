<script setup>
import LogIn from '../components/LogIn.vue'
import AnimalCards from '../components/AnimalCards.vue'
import SpikeCard from '../components/SpikeCard.vue'
import { trackSpikes } from '@/components/products'
</script>

<template>
  <main>
    <AnimalCards class="text-[50px]" />
    <div class="container flex flex-wrap gap-4 justify-center">
      <SpikeCard v-for="spike in trackSpikes" :spike="spike" :key="spike.name" />
    </div>

    <LogIn class="text-red-500" title="Help me" />
  </main>
</template>
