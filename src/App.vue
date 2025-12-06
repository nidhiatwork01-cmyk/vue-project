<template>
  <Navbar />
  <RouterView />
  <FooterComponent />
</template>

<script setup>
import Navbar from "./components/Navbar.vue";
import FooterComponent from "./components/FooterComponent.vue";
</script>

<style>
/* Optional layout styling */
body {
  margin: 0;
  padding: 0;
}
</style>
