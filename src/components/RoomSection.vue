<script setup lang="ts">
import HouseBlinds from './HouseBlinds.vue';
import HouseLamps from './HouseLamps.vue';
import HouseMusic from './HouseMusic.vue';
</script>

<template>
  <div class="panel-section">
    <div class="title-section">Control habitació</div>
    <br />
    <div class="section-items">
      <HouseLamps />
      <HouseBlinds />
      <HouseMusic />
    </div>
  </div>
</template>

<style></style>
