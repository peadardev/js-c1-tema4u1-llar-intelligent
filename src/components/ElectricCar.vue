<script setup lang="ts">
import { ref } from 'vue';
const percentatge = ref<number>(15);
const isRunning = ref<boolean>(false);
let interval: ReturnType<typeof setInterval> | null = null;

const startProgress = () => {
  if (interval) return;
  isRunning.value = true;
  interval = setInterval(() => {
    if (percentatge.value >= 100) {
      percentatge.value = 100;
      stopProgress();
    } else {
      percentatge.value++;
    }
  }, 500);
};

const stopProgress = () => {
  if (interval !== null) {
    clearInterval(interval);
    interval = null;
  }
  isRunning.value = false;
};

const toggleProgress = () => {
  if (isRunning.value) {
    stopProgress();
  } else {
    startProgress();
  }
};
</script>

<template>
  <div class="panel-item">
    <div>
      <div class="icon-unicode">🚗</div>
      <div class="title-item">Cotxe elèctric</div>
    </div>

    <div class="content-item">
      {{ isRunning ? 'Carregant' : 'Desconnectat' }}: {{ percentatge }}%
    </div>
    <div class="progress-bar">
      <div class="progress-fill" :style="{ width: percentatge + '%' }"></div>
    </div>
    <button @click="toggleProgress">
      {{ isRunning ? 'Desconnectar' : 'Connectar' }}
    </button>
  </div>
</template>

<style scoped>
.panel-item {
  background: orange;
}
.progress-bar {
  width: 100%;
  height: 20px;
  background: #ddd;
  border-radius: 5px;
  overflow: hidden;
}
.progress-fill {
  height: 100%;
  background: #42b883;
  transition: width 1s linear;
}
</style>
