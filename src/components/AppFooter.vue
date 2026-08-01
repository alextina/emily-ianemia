<script setup lang="ts">
import logo from '../assets/logo-sin-fondo.png'

const columns = [
  {
    title: 'Legal',
    links: ['Privacidad', 'Términos', 'Disclaimer Médico'],
  },
  {
    title: 'Contacto',
    links: ['Soporte', 'Email'],
  },
  {
    title: 'Proyecto',
    links: ['Hackathon 2024'],
  },
]
</script>

<template>
  <footer class="app-footer">
    <div class="app-footer__inner">
      <div class="app-footer__top">
        <div class="app-footer__brand">
          <div class="app-footer__logo-badge">
            <img :src="logo" alt="Emily" class="app-footer__logo" />
          </div>
          <p class="app-footer__tagline">
            Transformando la salud femenina a través de la conversación y el
            cuidado preventivo.
          </p>
        </div>

        <div class="app-footer__columns">
          <div v-for="column in columns" :key="column.title" class="app-footer__column">
            <h3 class="app-footer__column-title">{{ column.title }}</h3>
            <a v-for="link in column.links" :key="link" href="#" class="app-footer__link">
              {{ link }}
            </a>
          </div>
        </div>
      </div>

      <hr class="app-footer__divider" />

      <div class="app-footer__bottom">
        <span>© 2024 Emily Health. Reservados todos los derechos. Solo para fines educativos.</span>
        <span class="app-footer__made-with">
          <svg viewBox="0 0 24 24" width="14" height="14" fill="currentColor" aria-hidden="true">
            <path d="M12 21s-6.7-4.35-9.3-8.2C1 10.1 1.7 6.6 4.7 5.1c2-.98 4.2-.3 5.5 1.4L12 8.3l1.8-1.8c1.3-1.7 3.5-2.38 5.5-1.4 3 1.5 3.7 5 2 7.7C18.7 16.65 12 21 12 21Z" />
          </svg>
          Hecho con amor para el bienestar femenino.
        </span>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.app-footer {
  background: var(--brand-bg);
  border-top: 1px solid var(--brand-border);
  padding: 3.5rem 2rem 2rem;
}

.app-footer__inner {
  max-width: 1280px;
  margin: 0 auto;
}

.app-footer__top {
  display: flex;
  justify-content: space-between;
  gap: 3rem;
  margin-bottom: 2.5rem;
}

.app-footer__brand {
  max-width: 22rem;
}

.app-footer__logo-badge {
  display: inline-flex;
  align-items: center;
  background: #fff;
  border-radius: 10px;
  padding: 0.4rem 1rem;
  margin-bottom: 1rem;
}

.app-footer__logo {
  height: 20px;
  width: auto;
  display: block;
}

.app-footer__tagline {
  font-size: 0.9rem;
  line-height: 1.6;
  color: var(--brand-primary);
  margin: 0;
}

.app-footer__columns {
  display: flex;
  gap: 3.5rem;
}

.app-footer__column {
  display: flex;
  flex-direction: column;
  gap: 0.6rem;
}

.app-footer__column-title {
  font-size: 0.95rem;
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 0.3rem;
}

.app-footer__link {
  font-size: 0.88rem;
  color: var(--brand-primary);
  text-decoration: none;
}

.app-footer__link:hover {
  color: var(--brand-primary-dark);
}

.app-footer__divider {
  border: none;
  border-top: 1px solid var(--brand-border);
  margin: 0 0 1.5rem;
}

.app-footer__bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 0.75rem;
  font-size: 0.82rem;
  color: var(--brand-text-muted);
}

.app-footer__made-with {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  color: var(--brand-primary);
}

@media (max-width: 700px) {
  .app-footer__top {
    flex-direction: column;
  }

  .app-footer__columns {
    gap: 2rem;
  }
}
</style>
