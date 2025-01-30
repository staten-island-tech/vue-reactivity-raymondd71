<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import LogIn from '../components/LogIn.vue'
</script>

<template>
  <main>
    <TheWelcome />
    <LogIn class="text-red-500" message="I hate black berries" />
  </main>
</template>
