<script setup lang="ts">
import RoomSection from './components/RoomSection.vue';
import VehicleSection from './components/VehicleSection.vue';
</script>

<template>
  <div class="panel-general">
    <h3 class="title-panel">Panell general</h3>
    <RoomSection />
    <VehicleSection />
  </div>
</template>

<style>
.title-panel {
  padding: 0.5rem;
}
.panel-general {
  width: 44rem;
  font-family: Arial, sans-serif;
  border: 2px solid black;
  padding: 0.2rem;
  border-radius: 10px;
}
.panel-section {
  width: 40rem;
  border: 2px solid black;
  border-radius: 10px;
  padding: 0.5rem;
  margin: 1rem;
}
.section-items {
  display: flex;
}
.panel-item {
  width: 10rem;
  min-width: 10rem;
  height: 10rem;
  font-size: 16px;
  border: 1px solid blue;
  border-radius: 10px;
  padding: 1rem;
}
.title-section {
  font-size: 14;
  font-weight: bold;
}
.title-item {
  font-size: 14;
  font-weight: bold;
}
.content-item {
  font-size: 14px;
}
.icon-unicode {
  font-size: 1.5rem;
}
</style>
