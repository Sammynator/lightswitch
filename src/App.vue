<script setup>
import { ref } from "vue";

const isOn = ref(false);

function toggleClass() {
  isOn.value = !isOn.value;
}
</script>

<template>
  <div class="main">
    <div class="toggle">
      <h1 :class="{ on: isOn }">
        Turn me {{ isOn ? "off" : "on" }}
        <!-- Change text based on color -->
      </h1>
      <button @click="toggleClass"></button>
    </div>
  </div>
</template>
