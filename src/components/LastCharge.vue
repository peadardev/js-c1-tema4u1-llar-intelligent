<script setup lang="ts">
import { ref } from 'vue';
const energy = ref<number>(30);
const date = ref<string>(new Date().toLocaleDateString());
</script>

<template>
  <div class="panel-item">
    <div class="icon-unicode">⚡</div>
    <div class="title-item">Última càrrega</div>
    <div class="content-item">{{ energy }} kWh</div>
    <div class="content-item">{{ date }}</div>
  </div>
</template>

<style></style>
