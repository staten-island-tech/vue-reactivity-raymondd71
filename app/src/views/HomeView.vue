<script setup>
import LogIn from '../components/LogIn.vue'
import TitleHead from '../components/TitleHead.vue'
import SpikeCard from '../components/SpikeCard.vue'
import { trackSpikes } from '@/components/products'
import { cart } from '@/components/cart'
import CartList from '../components/CartList.vue'
</script>

<template>
  <main>
    <TitleHead class="text-[50px]" />
    <div class="container flex flex-wrap gap-4 justify-center">
      <SpikeCard v-for="spike in trackSpikes" :spike="spike" :key="spike.name" />
    </div>
    <div
      class="fixed top-0 right-0 w-[20%] h-full leading-4 p-4 flex flex-col overflow-y-scroll text-[1.5rem] border-1"
    >
      <h1 class="text-center">Shopping Cart</h1>
      <br />
      <hr />
      <CartList v-for="spike in cart" :spike="spike" :key="spike.name" />
    </div>
    <LogIn class="text-red-500" title="Help me" />
  </main>
</template>
