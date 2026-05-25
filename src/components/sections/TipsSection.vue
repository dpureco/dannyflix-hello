<template>
  <section id="tips" class="section">
    <div class="container">
      <p class="section-label">Get the most out of it</p>
      <h2 class="section-title">Tips & Tricks</h2>
      <p class="section-subtitle">
        A few settings worth changing and habits worth forming for the best experience.
      </p>

      <div class="tips-list">
        <div
          class="tip card"
          :class="{ 'tip--important': tip.important }"
          v-for="tip in tips"
          :key="tip.title"
        >
          <span class="tip-icon">{{ tip.icon }}</span>
          <div class="tip-body">
            <div class="tip-header">
              <h3 class="tip-title">{{ tip.title }}</h3>
              <span v-if="tip.important" class="tip-badge">Heads up</span>
            </div>
            <p class="tip-desc" v-html="tip.description"></p>
            <img v-if="tip.image" :src="tip.image" :alt="tip.imageAlt" class="tip-image" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const tips = [
  {
    icon: '🎬',
    title: 'Disable trailers & extras',
    description: 'Settings → Experience → untick <em>Show cinematic trailers</em> and <em>Show pre-play extras</em>. Stops Plex auto-playing trailers before your movie.',
  },
  {
    icon: '📺',
    title: 'Force original quality — on every device',
    important: true,
    description: 'Settings → Playback → set quality to <em>Original</em> (or <em>Maximum</em>). By default Plex may downgrade your stream to save bandwidth — this disables that. <strong>This setting is per-device</strong>, so you\'ll need to change it on every phone, TV, or computer you watch on.',
  },
  {
    icon: '⚡',
    title: 'Turn off auto quality adjustment',
    description: 'While you\'re in Playback settings, also disable <em>Automatically Adjust Quality</em>. It can aggressively drop the stream quality at the first sign of a hiccup.',
  },
  {
    icon: '▶️',
    title: 'Enable Direct Play',
    description: 'Settings → Playback → make sure <em>Allow Direct Play</em> and <em>Allow Direct Stream</em> are on. This plays files as-is without transcoding, giving you the best quality and zero server load.',
  },
  {
    icon: '🚫',
    title: 'Disable Plex\'s own streaming content',
    important: true,
    description: 'Plex quietly bundles its own free streaming service — movies, TV shows, and live TV that have nothing to do with this server. To turn it off: Settings → <em>Online Media Sources</em> → set every toggle to <em>Disabled</em>. This removes all of Plex\'s own content from your home screen and sidebar, leaving only the Dannyflix libraries.',
  },
  {
    icon: '🧹',
    title: 'Clean up your home screen',
    description: `Even after disabling Online Media Sources, the sidebar can still have leftover Plex items. Hover over any unwanted item and click <strong>✕</strong>, or right-click → <em>Unpin</em>. You can also drag sections around to reorder them — put the Dannyflix libraries front and centre.`,
    image: '/assets/images/nav_example.png',
    imageAlt: 'Example of the Plex sidebar showing Home, Watchlist, Movies and TV Shows',
  },
]
</script>

<style scoped>
.tips-list {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.tip {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  padding: 22px 24px;
  border-left: 3px solid transparent;
  transition: border-color 0.2s;
}

.tip--important {
  border-left-color: var(--accent);
  background: var(--surface-alt);
}

.tip-icon {
  font-size: 1.4rem;
  flex-shrink: 0;
  margin-top: 2px;
}

.tip-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 5px;
  flex-wrap: wrap;
}

.tip-title {
  font-size: 0.98rem;
  font-weight: 600;
  color: var(--text);
  margin: 0;
}

.tip-badge {
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--accent);
  background: color-mix(in srgb, var(--accent) 12%, transparent);
  border: 1px solid color-mix(in srgb, var(--accent) 30%, transparent);
  padding: 2px 8px;
  border-radius: 20px;
}

.tip-desc {
  font-size: 0.9rem;
  color: var(--text-muted);
  line-height: 1.6;
}

.tip-desc :deep(ul) {
  margin-top: 8px;
  padding-left: 18px;
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.tip-desc :deep(li) {
  line-height: 1.55;
}

.tip-image {
  margin-top: 14px;
  border-radius: 8px;
  border: 1px solid var(--border);
  max-width: 200px;
  box-shadow: var(--shadow);
}
</style>
