<script setup>
import { RouterView } from 'vue-router'
import MainNav from './components/navigation/MainNav.vue'
import MainFooter from './components/navigation/MainFooter.vue'
</script>

<template>
  <MainNav></MainNav>

  <RouterView />

  <MainFooter></MainFooter>
</template>

<style scoped>

</style>
