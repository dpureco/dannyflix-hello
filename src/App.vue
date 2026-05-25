<script setup>
import { ref, provide, onMounted } from 'vue'
import Navigation from '@/components/Navigation.vue'
import HeroSection from '@/components/sections/HeroSection.vue'
import GettingStartedSection from '@/components/sections/GettingStartedSection.vue'
import RequestsSection from '@/components/sections/RequestsSection.vue'
import TipsSection from '@/components/sections/TipsSection.vue'
import AlsoAvailableSection from '@/components/sections/AlsoAvailableSection.vue'

const dark = ref(false)

function toggleTheme() {
  dark.value = !dark.value
  document.documentElement.classList.toggle('dark', dark.value)
  localStorage.setItem('theme', dark.value ? 'dark' : 'light')
}

onMounted(() => {
  const saved = localStorage.getItem('theme')
  const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches
  dark.value = saved ? saved === 'dark' : prefersDark
  document.documentElement.classList.toggle('dark', dark.value)
})

provide('dark', dark)
provide('toggleTheme', toggleTheme)
</script>

<template>
  <Navigation />
  <main>
    <HeroSection />
    <GettingStartedSection />
    <RequestsSection />
    <TipsSection />
    <AlsoAvailableSection />
  </main>
  <footer class="site-footer">
    <div class="container">
      <p>Made with ♥ for the homies.</p>
    </div>
  </footer>
</template>

<style scoped>
main {
  padding-top: 64px;
}

.site-footer {
  background: var(--surface);
  border-top: 1px solid var(--border);
  padding: 28px 0;
  text-align: center;
  color: var(--text-muted);
  font-size: 0.875rem;
}
</style>
