<script setup lang="ts">
import heroImg from '../assets/hero-section-img.png'
</script>

<template>
  <div class="phone-mockup">
    <img :src="heroImg" alt="Emily chat en Telegram" class="phone-mockup__img" />
  </div>
</template>

<style scoped>
.phone-mockup {
  width: 100%;
  max-width: 480px;
}

.phone-mockup__img {
  display: block;
  width: 100%;
  height: auto;
}
</style>
