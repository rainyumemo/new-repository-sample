<template>
  <div id="app" class="min-h-screen bg-white">
    <TheNavigation />
    <main>
      <RouterView />
    </main>
    <TheFooter />
  </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import TheNavigation from './components/TheNavigation.vue'
import TheFooter from './components/TheFooter.vue'
</script>
