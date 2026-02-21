<template>
  <div class="landing">
    <!-- Background subtle noise/gradient overlay -->
    <div class="bg-overlay"></div>

    <!-- Logo -->
    <header class="header">
      <div class="logo">
        <PlanetIcon class="logo-icon" />
        <span class="logo-text">CEOS</span>
      </div>
    </header>

    <!-- Main content -->
    <main class="main">
      <h1 class="headline">Coming Soon</h1>
      <p class="subheadline">
        The framework to work with anything<br />
        using media.
      </p>
    </main>

    <!-- Footer -->
    <footer class="footer">
      <a
        href="https://github.com/enzotorrs/ceos"
        target="_blank"
        rel="noopener noreferrer"
        class="github-link"
      >
        <GitHubIcon class="github-icon" />
        <span>More information</span>
      </a>
    </footer>
  </div>
</template>

<script setup>
import PlanetIcon from './components/PlanetIcon.vue'
import GitHubIcon from './components/GitHubIcon.vue'
</script>

<style scoped>
.landing {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  padding: 2.5rem 2rem;
  position: relative;
  overflow: hidden;
}

.bg-overlay {
  position: absolute;
  inset: 0;
  background: radial-gradient(
    ellipse 60% 50% at 50% 0%,
    rgba(120, 60, 180, 0.06) 0%,
    transparent 70%
  );
  pointer-events: none;
  z-index: 0;
}

/* ---- Header ---- */
.header {
  z-index: 1;
  width: 100%;
  display: flex;
  justify-content: center;
  padding-top: 0.5rem;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.55rem;
}

.logo-icon {
  width: 4rem;
  height: 4rem;
}

.logo-text {
  font-size: 3.2rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  background: linear-gradient(135deg, #f4813f 0%, #c15de0 50%, #7b5cf0 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* ---- Main ---- */
.main {
  z-index: 1;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.2rem;
}

.headline {
  font-size: clamp(2.8rem, 6vw, 4.5rem);
  font-weight: 400;
  color: #f0f0f0;
  letter-spacing: -0.01em;
  line-height: 1.1;
}

.subheadline {
  font-size: clamp(1rem, 2vw, 1.2rem);
  font-weight: 300;
  color: #888899;
  line-height: 1.7;
  max-width: 480px;
}

/* ---- Footer ---- */
.footer {
  z-index: 1;
  padding-bottom: 0.5rem;
}

.github-link {
  display: flex;
  align-items: center;
  gap: 0.55rem;
  text-decoration: none;
  color: #c0c0cc;
  font-size: 1rem;
  font-weight: 400;
  transition: color 0.2s ease;
}

.github-link:hover {
  color: #ffffff;
}

.github-icon {
  width: 1.8rem;
  height: 1.8rem;
}
</style>
