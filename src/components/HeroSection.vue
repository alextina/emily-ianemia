<script setup lang="ts">
import PhoneMockup from './PhoneMockup.vue'
</script>

<template>
  <section class="hero">
    <div class="hero__inner">
      <div class="hero__content">
        <h1 class="hero__title">
          Tu ciclo, tu alimentación y tu energía,
          <span class="hero__title-accent">en un solo chat</span>
        </h1>

        <p class="hero__description">
          Emily te ayuda a prevenir la anemia ferropénica con seguimiento
          personalizado directamente en tu aplicación de mensajería favorita.
        </p>

        <a href="https://t.me/IAnemiabot" target="_blank" rel="noopener" class="hero__cta">
          <svg viewBox="0 0 24 24" width="18" height="18" fill="currentColor" aria-hidden="true">
            <path
              d="M21.05 3.53 2.9 10.55c-1.23.5-1.22 1.2-.22 1.5l4.65 1.45 1.8 5.5c.22.6.37.84.75.84.35 0 .5-.16.7-.36l1.7-1.63 4.7 3.44c.87.48 1.5.23 1.72-.8l3.1-14.4c.32-1.28-.5-1.86-1.55-1.56z"
            />
          </svg>
          Iniciar en Telegram
        </a>
      </div>

      <div class="hero__visual">
        <PhoneMockup />
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background: var(--brand-bg);
  padding: 5rem 2rem 6rem;
}

.hero__inner {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 3rem;
}

.hero__title {
  font-size: clamp(2rem, 4vw, 2.75rem);
  line-height: 1.2;
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 1.5rem;
}

.hero__title-accent {
  display: block;
  color: var(--brand-primary);
}

.hero__description {
  font-size: 1.05rem;
  line-height: 1.7;
  color: var(--brand-text-muted);
  max-width: 34rem;
  margin: 0 0 2.25rem;
}

.hero__cta {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  background: var(--brand-primary-dark);
  color: #fff;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  padding: 0.9rem 1.9rem;
  border-radius: 999px;
  transition: background 0.2s ease;
}

.hero__cta:hover {
  background: var(--brand-primary);
}

.hero__visual {
  display: flex;
  justify-content: center;
}

@media (max-width: 900px) {
  .hero__inner {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .hero__description {
    margin-left: auto;
    margin-right: auto;
  }

  .hero__visual {
    order: -1;
  }
}
</style>
