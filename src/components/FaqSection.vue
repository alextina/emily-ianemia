<script setup lang="ts">
import { ref } from 'vue'

const faqs = [
  {
    question: '¿Es Emily un sustituto del médico?',
    answer:
      'No. Emily es un asistente preventivo que te ayuda a identificar señales tempranas de anemia por falta de hierro, pero siempre recomienda acudir a un profesional de la salud para un diagnóstico.',
  },
  {
    question: '¿Mis datos están seguros en Telegram?',
    answer:
      'Sí. Tus conversaciones se manejan de forma privada y cifrada, y solo se usan para darte seguimiento y recomendaciones personalizadas.',
  },
  {
    question: '¿Cuánto cuesta usar Emily?',
    answer:
      'Emily es completamente gratuita durante esta etapa del proyecto.',
  },
  {
    question: '¿Qué necesito para empezar?',
    answer:
      'Solo una cuenta de Telegram. Busca @IAnemiabot o pulsa cualquier botón "Iniciar en Telegram" de esta página.',
  },
]

const openIndex = ref<number | null>(null)

function toggle(index: number) {
  openIndex.value = openIndex.value === index ? null : index
}
</script>

<template>
  <section id="faq" class="faq">
    <div class="faq__inner">
      <h2 class="faq__title">Preguntas frecuentes</h2>

      <div class="faq__list">
        <div v-for="(item, index) in faqs" :key="item.question" class="faq__item">
          <button
            type="button"
            class="faq__question"
            :aria-expanded="openIndex === index"
            @click="toggle(index)"
          >
            {{ item.question }}
            <svg
              class="faq__chevron"
              :class="{ 'faq__chevron--open': openIndex === index }"
              viewBox="0 0 24 24"
              width="18"
              height="18"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="m6 9 6 6 6-6" />
            </svg>
          </button>

          <p v-if="openIndex === index" class="faq__answer">{{ item.answer }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.faq {
  background: var(--brand-bg);
  padding: 5rem 2rem 6rem;
}

.faq__inner {
  max-width: 780px;
  margin: 0 auto;
}

.faq__title {
  text-align: center;
  font-size: clamp(1.5rem, 2.6vw, 2rem);
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 2.5rem;
}

.faq__list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.faq__item {
  background: #fff;
  border: 1px solid var(--brand-border);
  border-radius: 1rem;
  padding: 0.25rem 1.5rem;
}

.faq__question {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  background: none;
  border: none;
  cursor: pointer;
  text-align: left;
  font-family: inherit;
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--brand-heading);
  padding: 1.1rem 0;
}

.faq__chevron {
  flex-shrink: 0;
  color: var(--brand-text-muted);
  transition: transform 0.2s ease;
}

.faq__chevron--open {
  transform: rotate(180deg);
}

.faq__answer {
  margin: -0.25rem 0 1.1rem;
  font-size: 0.9rem;
  line-height: 1.6;
  color: var(--brand-text-muted);
}
</style>
