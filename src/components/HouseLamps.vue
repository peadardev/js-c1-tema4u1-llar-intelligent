<script setup lang="ts">
import { ref } from 'vue';
const percentatge = ref(50);
</script>

<template>
  <div class="panel-item">
    <div>
      <div class="icon-unicode">💡</div>
      <div class="title-item">Llums</div>
    </div>
    <div class="content-item">{{ percentatge }}%</div>
    <input type="range" min="0" max="100" v-model="percentatge" />
  </div>
</template>

<style></style>
