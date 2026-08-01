<script setup lang="ts">
const features = [
  {
    icon: 'calendar',
    iconBg: '#fbdcd2',
    iconColor: '#a85c46',
    title: 'Seguimiento de ciclo',
    description:
      'Registra tus días de flujo y recibe alertas personalizadas sobre tus niveles de energía.',
  },
  {
    icon: 'utensils',
    iconBg: '#d9ece4',
    iconColor: '#3f7a63',
    title: 'Tips de nutrición',
    description:
      'Análisis de tus comidas con sugerencias específicas de alimentos ricos en hierro.',
  },
  {
    icon: 'file-lines',
    iconBg: '#fbdcd2',
    iconColor: '#a85c46',
    title: 'Lectura de labs',
    description:
      'Sube una foto de tus análisis y Emily te ayudará a entender los indicadores clave.',
  },
  {
    icon: 'bell',
    iconBg: '#fbdcd2',
    iconColor: '#a85c46',
    title: 'Recordatorios',
    description:
      'Nunca olvides tu suplemento o tu cita médica con avisos gentiles en Telegram.',
  },
] as const
</script>

<template>
  <section class="features">
    <div class="features__inner">
      <div class="features__header">
        <h2 class="features__title">Diseñada para tu bienestar integral</h2>
        <p class="features__subtitle">
          Cuidado preventivo con la calidez de una amiga experta.
        </p>
      </div>

      <div class="features__grid">
        <div v-for="feature in features" :key="feature.title" class="feature-card">
          <div class="feature-card__icon" :style="{ background: feature.iconBg, color: feature.iconColor }">
            <svg v-if="feature.icon === 'calendar'" viewBox="0 0 24 24" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="4" width="18" height="18" rx="2" />
              <path d="M16 2v4M8 2v4M3 10h18" />
            </svg>
            <svg v-else-if="feature.icon === 'utensils'" viewBox="0 0 24 24" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M3 2v7c0 1.1.9 2 2 2s2-.9 2-2V2M5 11v11M15 2c-1.7 0-3 2.7-3 6s1.3 6 3 6 3-2.7 3-6-1.3-6-3-6ZM15 14v9" />
            </svg>
            <svg v-else-if="feature.icon === 'file-lines'" viewBox="0 0 24 24" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8Z" />
              <path d="M14 2v6h6M8 13h8M8 17h8M8 9h2" />
            </svg>
            <svg v-else-if="feature.icon === 'bell'" viewBox="0 0 24 24" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M6 8a6 6 0 0 1 12 0c0 7 3 9 3 9H3s3-2 3-9" />
              <path d="M10.3 21a1.94 1.94 0 0 0 3.4 0" />
            </svg>
          </div>

          <h3 class="feature-card__title">{{ feature.title }}</h3>
          <p class="feature-card__description">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.features {
  background: var(--brand-bg);
  padding: 5rem 2rem 6rem;
}

.features__inner {
  max-width: 1280px;
  margin: 0 auto;
}

.features__header {
  text-align: center;
  margin-bottom: 3rem;
}

.features__title {
  font-size: clamp(1.5rem, 2.6vw, 2rem);
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 0.75rem;
}

.features__subtitle {
  font-size: 1rem;
  color: var(--brand-text-muted);
  margin: 0;
}

.features__grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
}

.feature-card {
  background: transparent;
  border: 1px solid var(--brand-border);
  border-radius: 1.25rem;
  padding: 1.75rem 1.5rem;
}

.feature-card__icon {
  width: 44px;
  height: 44px;
  border-radius: 0.75rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.25rem;
}

.feature-card__title {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 0.5rem;
}

.feature-card__description {
  font-size: 0.9rem;
  line-height: 1.6;
  color: var(--brand-text-muted);
  margin: 0;
}

@media (max-width: 900px) {
  .features__grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 560px) {
  .features__grid {
    grid-template-columns: 1fr;
  }
}
</style>
