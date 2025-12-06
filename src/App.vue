<template>
  <div class="app-shell">
    <Navbar />

    <main class="app-main">
      <div class="container">
        <RouterView />
      </div>
    </main>

    <FooterComponent />
  </div>
</template>


<script setup lang="ts">
import { RouterView } from "vue-router";
import Navbar from "./components/Navbar.vue";
import FooterComponent from "./components/FooterComponent.vue";
</script>

<style scoped>
.app-shell {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background: radial-gradient(circle at top, #111827 0, #020617 60%);
  color: var(--text);
}


.app-main {
  flex: 1;
  width: 100%;
  margin: 0 auto;
  padding: 1.5rem 1.25rem 2.5rem;
}

/* Desktop spacing */
@media (min-width: 768px) {
  .app-main {
    padding: 2.5rem 1.5rem 3rem;
  }
}
</style>
