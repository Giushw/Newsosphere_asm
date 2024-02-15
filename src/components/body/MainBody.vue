<template>
    <main class="body">
      <TbaContent />
    </main>
  </template>
  
  <script setup lang="ts">
    import TbaContent from '../common/TbaContent.vue';
  </script>
  
  <style lang="scss">
    .body {
      @apply font-raleway flex h-[60vh] w-full flex-col;
    }
  </style>