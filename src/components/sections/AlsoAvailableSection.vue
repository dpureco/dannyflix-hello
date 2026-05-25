<template>
  <section id="also-available" class="section" style="background: var(--bg-alt)">
    <div class="container">
      <p class="section-label">There's more</p>
      <h2 class="section-title">Also Available</h2>
      <p class="section-subtitle">
        Dannyflix isn't just movies and TV — here's what else is on offer.
      </p>

      <div class="card-grid">
        <div class="card also-card">
          <span class="also-icon">🎧</span>
          <h3>Audiobooks</h3>
          <p>
            There's a separate audiobook library available. It runs on its own platform
            and requires a separate login — just reach out and I'll get you set up.
          </p>
        </div>
        <div class="card also-card">
          <span class="also-icon">🔧</span>
          <h3>Something not working?</h3>
          <p>
            Bad video quality, wrong audio track, missing episode — whatever it is,
            just reach out and I'll take a look.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.also-card {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.also-icon { font-size: 1.8rem; }

.also-card h3 {
  font-size: 1rem;
  font-weight: 600;
  color: var(--text);
}

.also-card p {
  font-size: 0.92rem;
  color: var(--text-muted);
  line-height: 1.6;
}
</style>
