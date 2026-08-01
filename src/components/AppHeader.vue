<script setup lang="ts">
import logo from '../assets/logo-sin-fondo.png'

const navLinks = [
  { label: 'Features', href: '#features' },
  { label: 'How it Works', href: '#how-it-works' },
  { label: 'FAQ', href: '#faq' },
]
</script>

<template>
  <header class="app-header">
    <div class="app-header__inner">
      <div class="app-header__brand-group">
        <a href="#" class="app-header__brand">
          <img :src="logo" alt="Emily" class="app-header__logo" />
        </a>
        <span class="app-header__slogan">Tu confidente de salud femenina</span>
      </div>

      <nav class="app-header__nav">
        <a v-for="link in navLinks" :key="link.href" :href="link.href" class="app-header__link">
          {{ link.label }}
        </a>
      </nav>

      <a href="https://t.me/IAnemiabot" target="_blank" rel="noopener" class="app-header__cta">Talk to Emily</a>
    </div>
  </header>
</template>

<style scoped>
.app-header {
  border-bottom: 1px solid var(--brand-border);
  background: var(--brand-bg);
}

.app-header__inner {
  max-width: 1280px;
  margin: 0 auto;
  padding: 1.25rem 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
}

.app-header__brand-group {
  display: flex;
  align-items: center;
  gap: 0.9rem;
}

.app-header__brand {
  display: inline-flex;
  align-items: center;
  background: #fff;
  border-radius: 10px;
  padding: 0.4rem 1rem;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.04);
}

.app-header__logo {
  height: 22px;
  width: auto;
  display: block;
}

.app-header__slogan {
  font-size: 0.82rem;
  font-style: italic;
  color: var(--brand-text-muted);
  white-space: nowrap;
}

.app-header__nav {
  display: flex;
  align-items: center;
  gap: 2.5rem;
  flex: 1;
  justify-content: center;
}

.app-header__link {
  color: var(--brand-heading);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
  transition: color 0.2s ease;
}

.app-header__link:hover {
  color: var(--brand-primary);
}

.app-header__cta {
  display: inline-flex;
  align-items: center;
  white-space: nowrap;
  background: var(--brand-primary-dark);
  color: #fff;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.9rem;
  padding: 0.7rem 1.5rem;
  border-radius: 999px;
  transition: background 0.2s ease;
}

.app-header__cta:hover {
  background: var(--brand-primary);
}

@media (max-width: 900px) {
  .app-header__slogan {
    display: none;
  }
}

@media (max-width: 768px) {
  .app-header__nav {
    display: none;
  }
}
</style>
