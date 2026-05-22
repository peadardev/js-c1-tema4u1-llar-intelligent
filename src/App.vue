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
button {
  width: 5rem;
  height: 1.5rem;
  font-size: 12px;
  cursor: pointer;
  background: lightblue;
  padding: 1px;
  border: 0.5px solid darkgray;
  border-radius: 5px;
}
.title-panel {
  padding: 0.5rem;
}
.panel-general {
  width: 44rem;
  font-family: Arial, sans-serif;
  background: lightgrey;
  border: 1px solid black;
  padding: 0.2rem;
  border-radius: 10px;
}
.panel-section {
  width: 40rem;
  background: white;
  border: 1px solid darkgray;
  border-radius: 10px;
  padding: 0.5rem;
  margin: 1rem;
}
.section-items {
  display: flex;
}
.panel-item {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 10rem;
  min-width: 10rem;
  height: 10rem;
  font-size: 16px;
  background: lightyellow;
  border: 0px solid darkgrey;
  border-radius: 10px;
  padding: 1rem;
  margin: 0.5rem;
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
