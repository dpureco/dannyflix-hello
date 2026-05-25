<template>
  <section id="requests" class="section">
    <div class="container">
      <p class="section-label">Want something added?</p>
      <h2 class="section-title">Requesting Content</h2>
      <p class="section-subtitle">
        Don't see what you're looking for? Request it and it'll be added automatically —
        most things show up within minutes.
      </p>

      <div class="request-cta card">
        <div class="cta-text">
          <h3>Movies & TV Shows</h3>
          <p>Search for anything — movies, series, specific seasons. New episodes are grabbed automatically as they air.</p>
        </div>
        <a href="https://request.dannynet.org" class="btn btn-primary" target="_blank" rel="noopener">
          Open Request Portal →
        </a>
      </div>

      <div class="auth-note card">
        <span class="auth-icon">🔐</span>
        <p>The request portal uses your <strong>Plex account</strong> to sign in — just click <em>Sign in with Plex</em> and it'll authenticate through Plex directly. No separate account needed.</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.btn-primary {
  background: #e2c799;
  color: #0c2a3d;
}
.btn-primary:hover {
  background: #d4b47f;
  color: #0c2a3d;
}
.request-cta {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  flex-wrap: wrap;
}

.cta-text h3 {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--text);
  margin-bottom: 6px;
}

.cta-text p {
  font-size: 0.95rem;
  color: var(--text-muted);
  max-width: 480px;
}

.auth-note {
  display: flex;
  align-items: flex-start;
  gap: 14px;
  margin-top: 16px;
  background: var(--surface-alt);
}

.auth-icon { font-size: 1.1rem; flex-shrink: 0; margin-top: 2px; }

.auth-note p {
  font-size: 0.9rem;
  color: var(--text-muted);
  line-height: 1.6;
}
</style>
