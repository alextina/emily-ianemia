<script setup lang="ts">
const steps = [
  {
    number: 1,
    title: 'Abre el chat',
    description: 'Busca @EmilyBot en Telegram o pulsa los botones de esta web.',
  },
  {
    number: 2,
    title: 'Cuéntale tu ciclo',
    description: 'Emily te hará unas preguntas breves para entender tu ritmo actual.',
  },
  {
    number: 3,
    title: 'Recibe recomendaciones',
    description: 'Obtén planes de alimentación y alertas preventivas en tiempo real.',
  },
  {
    number: 4,
    title: 'Prepárate para tu médico',
    description: 'Genera reportes fáciles de leer para tu próxima consulta ginecológica.',
  },
]

// import howItWorksPhoto from '../assets/how-it-works.png'
</script>

<template>
  <section id="how-it-works" class="how-it-works">
    <div class="how-it-works__inner">
      <div class="how-it-works__visual">
        <!-- <img :src="howItWorksPhoto" alt="Chat con Emily en Telegram" /> -->
        <span class="how-it-works__visual-label">Imagen pendiente</span>
      </div>

      <div class="how-it-works__content">
        <h2 class="how-it-works__title">Cómo empezar tu camino con Emily</h2>

        <ol class="how-it-works__steps">
          <li v-for="step in steps" :key="step.number" class="how-it-works__step">
            <span class="how-it-works__step-number">{{ step.number }}</span>
            <div>
              <h3 class="how-it-works__step-title">{{ step.title }}</h3>
              <p class="how-it-works__step-description">{{ step.description }}</p>
            </div>
          </li>
        </ol>

        <a href="#chat" class="how-it-works__cta">Empezar ahora</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.how-it-works {
  background: var(--brand-bg-soft);
  padding: 5rem 2rem;
}

.how-it-works__inner {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 4rem;
}

.how-it-works__visual {
  aspect-ratio: 4 / 3.4;
  border-radius: 1.5rem;
  background: #ece8e4;
  border: 2px dashed var(--brand-border);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--brand-text-muted);
  font-size: 0.9rem;
}

.how-it-works__title {
  font-size: clamp(1.5rem, 2.6vw, 2rem);
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 2rem;
}

.how-it-works__steps {
  list-style: none;
  margin: 0 0 2.5rem;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 1.75rem;
}

.how-it-works__step {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.how-it-works__step-number {
  flex-shrink: 0;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  background: var(--brand-primary-dark);
  color: #fff;
  font-weight: 700;
  font-size: 0.9rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.how-it-works__step-title {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 0.35rem;
}

.how-it-works__step-description {
  font-size: 0.92rem;
  line-height: 1.6;
  color: var(--brand-text-muted);
  margin: 0;
}

.how-it-works__cta {
  display: inline-flex;
  align-items: center;
  background: var(--brand-green-dark);
  color: #fff;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.95rem;
  padding: 0.85rem 1.9rem;
  border-radius: 999px;
  transition: opacity 0.2s ease;
}

.how-it-works__cta:hover {
  opacity: 0.9;
}

@media (max-width: 900px) {
  .how-it-works__inner {
    grid-template-columns: 1fr;
  }
}
</style>
