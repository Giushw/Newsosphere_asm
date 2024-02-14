<template>
    <footer class="footer">
      <FooterAnchors />
    </footer>
  </template>
  
  <script setup lang="ts">
    import FooterAnchors from './FooterAnchors.vue';
  </script>
  
  <style lang="scss">
    .footer {
      @apply font-anybody flex w-full flex-col;
    }
  </style>