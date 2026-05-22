<script setup lang="ts">
import { ref } from 'vue';
const isPlaying = ref<boolean>(true);
const togglePlay = () => {
  isPlaying.value = !isPlaying.value;
};
const playNextSong = () => {
  isPlaying.value = true;
};
</script>

<template>
  <div class="panel-item">
    <div>
      <div class="icon-unicode">🎵</div>
      <div class="title-item">Música</div>
    </div>
    <div class="content-item">{{ isPlaying ? 'Reproduint' : 'Pausat' }}</div>
    <div>
      <span>
        <button @click="togglePlay">{{ isPlaying ? 'Pausar' : 'Reproduir' }}</button>
        <button @click="playNextSong">Següent</button>
      </span>
    </div>
  </div>
</template>

<style scoped>
.panel-item {
  background: lightgoldenrodyellow;
}
</style>
