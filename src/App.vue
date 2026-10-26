<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
const marker = 'FIGMA_WEB_BASELINE_20261026'
</script>

<template>
  <main class="page">
    <h1>Figma Make Web Test</h1>
    <p class="subtitle">
      A minimal Vue 3 + Vite + TypeScript baseline for testing AI coding agents.
    </p>

    <button type="button" class="counter" data-testid="counter-button" @click="count++">
      Count is {{ count }}
    </button>

    <p class="marker">
      Baseline marker: <code data-testid="baseline-marker">{{ marker }}</code>
    </p>
  </main>
</template>
