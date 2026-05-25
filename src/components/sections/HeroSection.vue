<template>
  <section class="hero">
    <div class="container">
      <p class="hero-eyebrow">You're in. Welcome.</p>
      <h1 class="hero-title">Welcome to<br />Dannyflix.</h1>
      <p class="hero-sub">
        You've been granted access to the server. This page covers everything
        you need to get set up and start watching.
      </p>
      <div class="hero-actions">
        <a href="#getting-started" class="btn btn-primary">Get Started →</a>
        <a href="#requests" class="btn btn-outline">Request Content</a>
      </div>
    </div>
    <div class="hero-wave" aria-hidden="true">
      <svg viewBox="0 0 1440 80" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M0,40 C360,80 1080,0 1440,40 L1440,80 L0,80 Z" fill="var(--bg-alt)" />
      </svg>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  background: linear-gradient(135deg, #0c4a6e 0%, #0f766e 100%);
  padding: 100px 0 0;
  overflow: hidden;
}

.hero-eyebrow {
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.75);
  margin-bottom: 16px;
}

.hero-title {
  font-size: clamp(2.2rem, 5vw, 3.4rem);
  font-weight: 700;
  color: #fff;
  line-height: 1.15;
  margin-bottom: 20px;
}

.hero-sub {
  font-size: 1.1rem;
  color: rgba(255,255,255,0.85);
  max-width: 520px;
  margin-bottom: 36px;
  line-height: 1.7;
}

.hero-actions {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  margin-bottom: 64px;
}

.hero-actions .btn-primary {
  background: #bae6fd;
  color: #0c2a3d;
}
.hero-actions .btn-primary:hover {
  background: #7dd3fc;
  color: #0c2a3d;
}
.hero-actions .btn-outline {
  background: #5eead4;
  color: #0c2a1e;
  border-color: transparent;
}
.hero-actions .btn-outline:hover {
  background: #2dd4bf;
  color: #0c2a1e;
}

.hero-wave {
  line-height: 0;
  margin-bottom: -2px;
}
.hero-wave svg {
  width: 100%;
  height: 80px;
  display: block;
}
</style>
