<script setup lang="ts">
import phoneMockup from '../assets/phone-mockup.png'
</script>

<template>
  <div class="phone-mockup">
    <img :src="phoneMockup" alt="Emily chat en Telegram" class="phone-mockup__img" />
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
