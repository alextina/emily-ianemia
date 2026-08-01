<script setup lang="ts"></script>

<template>
  <section class="trust">
    <div class="trust__card">
      <svg class="trust__icon" viewBox="0 0 24 24" width="28" height="28" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10Z" />
        <path d="m9 12 2 2 4-4" />
      </svg>

      <h2 class="trust__title">Tu salud es lo primero</h2>

      <p class="trust__description">
        "Emily no reemplaza a tu médico". Nuestra misión es educar y
        acompañar, pero siempre fomentamos la consulta profesional. Tus datos
        están cifrados y tu privacidad es nuestra prioridad absoluta.
      </p>

    </div>
  </section>
</template>

<style scoped>
.trust {
  background: var(--brand-bg);
  padding: 5rem 2rem 6rem;
}

.trust__card {
  max-width: 840px;
  margin: 0 auto;
  background: var(--brand-bg-soft);
  border-radius: 1.5rem;
  padding: 3rem 2rem;
  text-align: center;
}

.trust__icon {
  color: var(--brand-primary-dark);
  margin-bottom: 1rem;
}

.trust__title {
  font-size: 1.4rem;
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 1rem;
}

.trust__description {
  font-size: 0.95rem;
  line-height: 1.7;
  color: var(--brand-text-muted);
  max-width: 40rem;
  margin: 0 auto 1.75rem;
}

.trust__badges {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.trust__badge {
  width: 96px;
  height: 40px;
  border-radius: 0.5rem;
  background: #ddd8d3;
}
</style>
