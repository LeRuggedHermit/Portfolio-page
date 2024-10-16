<script setup>
import { RouterView } from 'vue-router'
import siteHeader from './components/Header.vue'
import siteBanner_1 from './components/Hero.vue'
import siteFooter from './components/Footer.vue'
</script>

<template>
  <siteHeader />
<siteBanner_1 />
  <RouterView />
  <siteFooter />
</template>

<style scoped>

</style>
