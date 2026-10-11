<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

const { currentPage, total } = useNav()

// Oculta la barra/footer en portada (1) y en slides de sección/center
const progress = computed(() => (currentPage.value / total.value) * 100)
</script>

<template>
  <!-- Barra de progreso -->
  <div class="global-progress">
    <div class="global-progress-bar" :style="{ width: progress + '%' }" />
  </div>

  <!-- Footer con marca y numeración -->
  <div class="global-footer">
    <div class="global-footer-brand">
      <span class="global-footer-dot" />
      TecIlia · CRUD con Spring Boot y JPA
    </div>
    <div class="global-footer-page">
      {{ currentPage }} / {{ total }}
    </div>
  </div>
</template>

<style scoped>
.global-progress {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 3px;
  background: rgba(0, 0, 0, 0.06);
  z-index: 50;
}

.global-progress-bar {
  height: 100%;
  background: linear-gradient(90deg, #2563eb, #06b6d4);
  transition: width 0.3s ease;
}

.global-footer {
  position: fixed;
  bottom: 10px;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  font-size: 11px;
  color: rgba(100, 116, 139, 0.7);
  z-index: 50;
  pointer-events: none;
}

.global-footer-brand {
  display: flex;
  align-items: center;
  gap: 6px;
  letter-spacing: 0.03em;
}

.global-footer-dot {
  width: 7px;
  height: 7px;
  border-radius: 999px;
  background: linear-gradient(90deg, #2563eb, #06b6d4);
  display: inline-block;
}

.global-footer-page {
  font-variant-numeric: tabular-nums;
  font-weight: 600;
}
</style>
