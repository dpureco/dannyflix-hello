<template>
  <section id="getting-started" class="section" style="background: var(--bg-alt)">
    <div class="container">
      <p class="section-label">Step by step</p>
      <h2 class="section-title">Getting Started</h2>
      <p class="section-subtitle">
        Follow these steps to get set up. It only takes a few minutes.
      </p>

      <div class="steps">
        <div class="step card" v-for="step in steps" :key="step.number">
          <div class="step-number">{{ step.number }}</div>
          <div>
            <h3 class="step-title">{{ step.title }}</h3>
            <p class="step-desc">{{ step.description }}</p>
            <a v-if="step.link" :href="step.link" :target="step.link.startsWith('#') ? '_self' : '_blank'" class="step-link">
              {{ step.linkText }} →
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  {
    number: '01',
    title: 'Download Plex',
    description: 'Plex is available on pretty much every device — phones, smart TVs, consoles, browsers, you name it.',
    link: 'https://www.plex.tv/media-server-downloads/#plex-app',
    linkText: 'Download Plex',
  },
  {
    number: '02',
    title: 'Create a Plex Account',
    description: 'You\'ll need a free Plex account to sign in. Use the email address your invite was sent to.',
    link: 'https://www.plex.tv/sign-up',
    linkText: 'Sign up for free',
  },
  {
    number: '03',
    title: 'Accept the Invite',
    description: 'Check your email for a sharing invite from the server. Click accept and you\'re in — the library will appear automatically.',
    link: null,
    linkText: null,
  },
  {
    number: '04',
    title: 'Start Watching',
    description: 'Open Plex, navigate to the shared libraries, and enjoy. Don\'t see something you want? You can request it.',
    link: null,
    linkText: null,
  },
  {
    number: '05',
    title: 'Tweak a Few Settings',
    description: 'Before you get too comfortable — take two minutes to check the tips below. A couple of settings make a real difference to your experience, and one in particular is worth doing right away.',
    link: '#tips',
    linkText: 'Read the tips',
  },
]
</script>

<style scoped>
.steps {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.step {
  display: flex;
  align-items: flex-start;
  gap: 24px;
}

.step-number {
  font-size: 1.6rem;
  font-weight: 700;
  color: var(--primary);
  opacity: 0.5;
  min-width: 48px;
  line-height: 1;
  padding-top: 2px;
}

.step-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--text);
  margin-bottom: 6px;
}

.step-desc {
  font-size: 0.95rem;
  color: var(--text-muted);
  margin-bottom: 10px;
}

.step-link {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--primary);
}
</style>
