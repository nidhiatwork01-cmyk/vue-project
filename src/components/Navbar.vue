<template>
  <nav class="nav">
    <router-link to="/" class="item">Home</router-link>
    <router-link to="/projects" class="item">Projects</router-link>
    <router-link to="/about" class="item">About</router-link>

    <button class="mode-btn" @click="toggleTheme">
      {{ theme === 'dark' ? '🌙 Dark' : '☀️ Light' }}
    </button>
  </nav>
</template>

<script setup>
import { ref, onMounted } from "vue";

const theme = ref("dark");

onMounted(() => {
  const savedTheme = localStorage.getItem("theme");
  if (savedTheme) {
    theme.value = savedTheme;
  }
  document.body.className = theme.value;
});

function toggleTheme() {
  theme.value = theme.value === "dark" ? "light" : "dark";
  document.body.className = theme.value;
  localStorage.setItem("theme", theme.value);
}
</script>

<style>
.nav {
  background: #111;
  padding: 15px;
  text-align: center;
}

.item {
  color: white;
  margin: 0 12px;
  font-size: 18px;
  text-decoration: none;
}

.item:hover {
  text-decoration: underline;
}

.mode-btn {
  background: #00eaff;
  padding: 7px 12px;
  border-radius: 12px;
  border: none;
  margin-left: 15px;
  cursor: pointer;
  color: black;
  font-weight: 600;
}

/* MAIN THEME SWITCH */
body.dark {
  background: #0e0e0e;
  color: white;
}

body.light {
  background: #f3f3f3;
  color: black;
}
</style>

