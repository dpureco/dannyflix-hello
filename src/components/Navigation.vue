<script setup>
import { inject } from 'vue'

const dark = inject('dark')
const toggleTheme = inject('toggleTheme')
</script>

<template>
  <nav class="nav">
    <div class="container nav-inner">
      <a href="#" class="nav-brand">🎬 Dannyflix</a>

      <ul class="nav-links">
        <li><a href="#getting-started">Getting Started</a></li>
        <li><a href="#requests">Requests</a></li>
        <li><a href="#tips">Tips</a></li>
        <li><a href="#also-available">Also Available</a></li>
      </ul>

      <button class="theme-toggle" @click="toggleTheme" :aria-label="dark ? 'Switch to light mode' : 'Switch to dark mode'">
        <span v-if="dark">☀️</span>
        <span v-else>🌙</span>
      </button>
    </div>
  </nav>
</template>

<style scoped>
.nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  height: 64px;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  box-shadow: var(--shadow);
  backdrop-filter: blur(8px);
}

.nav-inner {
  display: flex;
  align-items: center;
  height: 100%;
  gap: 32px;
}

.nav-brand {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--text);
  text-decoration: none;
  white-space: nowrap;
}
.nav-brand:hover { color: var(--primary); text-decoration: none; }

.nav-links {
  display: flex;
  list-style: none;
  gap: 24px;
  flex: 1;
}

.nav-links a {
  font-size: 0.9rem;
  font-weight: 500;
  color: var(--text-muted);
  transition: color 0.15s;
}
.nav-links a:hover { color: var(--primary); text-decoration: none; }

.theme-toggle {
  margin-left: auto;
  background: var(--surface-alt);
  border: 1px solid var(--border);
  border-radius: 8px;
  width: 38px;
  height: 38px;
  font-size: 1rem;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background 0.18s;
  flex-shrink: 0;
}
.theme-toggle:hover { background: var(--bg-alt); }

@media (max-width: 600px) {
  .nav-links { display: none; }
}
</style>
