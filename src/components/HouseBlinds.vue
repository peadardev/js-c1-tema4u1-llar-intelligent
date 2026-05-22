<script setup lang="ts">
import { ref } from 'vue';
const isOpen = ref<boolean>(true);
const toggleStatus = () => {
  isOpen.value = !isOpen.value;
};
</script>

<template>
  <div class="panel-item">
    <div>
      <div class="icon-unicode">{{ isOpen ? '🔲' : '🔳' }}</div>
      <div class="title-item">Persianes</div>
    </div>
    <div class="content-item">{{ isOpen ? 'Obertes' : 'Tancades' }}</div>
    <button @click="toggleStatus">{{ isOpen ? 'Tancar' : 'Obrir' }}</button>
  </div>
</template>

<style scoped>
.panel-item {
  background: lightcyan;
}
</style>
