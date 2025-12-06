<template>
  <header class="nav-wrapper">
    <nav class="nav">
      <div class="nav-left">
        <a href="/" class="nav-logo">nidhi.dev</a>
      </div>

      <!-- Desktop links -->
      <ul class="nav-links nav-links--desktop">
        <li><RouterLink to="/" class="nav-link" exact-active-class="nav-link--active">Home</RouterLink></li>
        <li><RouterLink to="/projects" class="nav-link" active-class="nav-link--active">Projects</RouterLink></li>
        <li><RouterLink to="/about" class="nav-link" active-class="nav-link--active">About</RouterLink></li>
      </ul>

      <div class="nav-right">
        <button class="icon-btn" @click="toggleTheme" :aria-label="isDark ? 'Switch to light mode' : 'Switch to dark mode'">
          <span v-if="isDark">🌙</span>
          <span v-else>☀️</span>
        </button>

        <!-- Mobile menu button -->
        <button class="icon-btn nav-menu-btn" @click="isMenuOpen = !isMenuOpen" aria-label="Toggle navigation menu">
          <span v-if="!isMenuOpen">☰</span>
          <span v-else>✕</span>
        </button>
      </div>
    </nav>

    <!-- Mobile menu -->
    <transition name="slide-fade">
      <ul v-if="isMenuOpen" class="nav-links nav-links--mobile">
        <li><RouterLink @click="closeMenu" to="/" class="nav-link" exact-active-class="nav-link--active">Home</RouterLink></li>
        <li><RouterLink @click="closeMenu" to="/projects" class="nav-link" active-class="nav-link--active">Projects</RouterLink></li>
        <li><RouterLink @click="closeMenu" to="/about" class="nav-link" active-class="nav-link--active">About</RouterLink></li>
      </ul>
    </transition>
  </header>
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue";
import { RouterLink } from "vue-router";

const isDark = ref(true);
const isMenuOpen = ref(false);

const applyTheme = () => {
  const body = document.body;
  body.classList.remove("light", "dark");
  body.classList.add(isDark.value ? "dark" : "light");
};

const toggleTheme = () => {
  isDark.value = !isDark.value;
  applyTheme();
  localStorage.setItem("theme", isDark.value ? "dark" : "light");
};

const closeMenu = () => {
  isMenuOpen.value = false;
};

onMounted(() => {
  const saved = localStorage.getItem("theme");
  if (saved === "light") isDark.value = false;
  applyTheme();
});
</script>

<style scoped>
.nav-wrapper {
  position: sticky;
  top: 0;
  z-index: 40;
  backdrop-filter: blur(14px);
  background: linear-gradient(to bottom, rgba(15, 23, 42, 0.85), rgba(15, 23, 42, 0.7));
  border-bottom: 1px solid rgba(148, 163, 184, 0.25);
}

.nav {
  max-width: 1120px;
  margin: 0 auto;
  padding: 0.85rem 1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  font-size: 0.95rem;
  color: var(--accent);
  text-decoration: none;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.nav-links--desktop {
  display: none;
}

.nav-link {
  font-size: 0.9rem;
  text-decoration: none;
  color: #e5e7eb;
  padding: 0.4rem 0.8rem;
  border-radius: 999px;
  opacity: 0.8;
  transition: 0.2s ease;
}

.nav-link:hover {
  opacity: 1;
  background: rgba(148, 163, 184, 0.15);
}

.nav-link--active {
  background: rgba(0, 234, 255, 0.16);
  color: var(--accent);
  opacity: 1;
}

.nav-right {
  display: flex;
  align-items: center;
  gap: 0.3rem;
}

.icon-btn {
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.4);
  background: rgba(15, 23, 42, 0.8);
  padding: 0.35rem 0.55rem;
  font-size: 0.9rem;
  cursor: pointer;
  display: flex;
  align-items: center;
}

.icon-btn:hover {
  border-color: var(--accent);
}

.nav-menu-btn {
  display: inline-flex;
  font-size: 1rem;
}

/* Mobile menu */
.nav-links--mobile {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  padding: 0.75rem 1.25rem 1rem;
  border-top: 1px solid rgba(148, 163, 184, 0.3);
  background: rgba(15, 23, 42, 0.98);
}

.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: opacity 0.18s ease, transform 0.18s ease;
}
.slide-fade-enter-from,
.slide-fade-leave-to {
  opacity: 0;
  transform: translateY(-6px);
}

/* Desktop */
@media (min-width: 768px) {
  .nav {
    padding-inline: 1.5rem;
  }

  .nav-links--desktop {
    display: flex;
  }

  .nav-links--mobile,
  .nav-menu-btn {
    display: none;
  }
}
</style>
