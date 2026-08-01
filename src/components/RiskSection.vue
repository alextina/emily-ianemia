<script setup lang="ts"></script>

<template>
  <section class="risk">
    <div class="risk__inner">
      <div class="risk__content">
        <span class="risk__badge">Un riesgo silencioso</span>

        <h2 class="risk__title">
          La pérdida de hierro durante el ciclo no debe ignorarse
        </h2>

        <p class="risk__description">
          Sentir fatiga constante, falta de aire o palidez puede ser señal de
          algo más. Durante el periodo, nuestro cuerpo pierde reservas vitales
          que impactan directamente en nuestra energía diaria.
        </p>
      </div>

      <div class="risk__stat-card">
        <div class="risk__stat-number">1 de cada 3</div>
        <div class="risk__stat-label">mujeres en edad fértil</div>
        <p class="risk__stat-description">
          sufren de deficiencia de hierro en el mundo.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.risk {
  background: var(--brand-bg);
  padding: 5rem 2rem;
}

.risk__inner {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 3rem;
}

.risk__badge {
  display: inline-block;
  background: #fbdcd2;
  color: var(--brand-primary-dark);
  font-size: 0.8rem;
  font-weight: 600;
  padding: 0.4rem 0.9rem;
  border-radius: 999px;
  margin-bottom: 1.25rem;
}

.risk__title {
  font-size: clamp(1.5rem, 2.6vw, 2rem);
  line-height: 1.3;
  font-weight: 700;
  color: var(--brand-heading);
  margin: 0 0 1.25rem;
}

.risk__description {
  font-size: 1rem;
  line-height: 1.7;
  color: var(--brand-text-muted);
  max-width: 32rem;
  margin: 0;
}

.risk__stat-card {
  background: #fff;
  border-radius: 1.5rem;
  padding: 3rem 2.5rem;
  box-shadow: 0 20px 40px -20px rgba(0, 0, 0, 0.12);
  text-align: center;
}

.risk__stat-number {
  font-size: clamp(2.5rem, 4vw, 3.25rem);
  font-weight: 800;
  color: var(--brand-primary-dark);
  margin-bottom: 0.75rem;
}

.risk__stat-label {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--brand-heading);
  margin-bottom: 0.5rem;
}

.risk__stat-description {
  font-size: 0.9rem;
  color: var(--brand-text-muted);
  margin: 0;
}

@media (max-width: 900px) {
  .risk__inner {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .risk__description {
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
