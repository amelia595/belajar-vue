<script setup>
import { RouterView } from 'vue-router'
import { Footer, Header } from './components'
</script>

<template>
  <Header class="fixed top-0 left-0 right-0" />
  <RouterView />
  <Footer />
</template>
