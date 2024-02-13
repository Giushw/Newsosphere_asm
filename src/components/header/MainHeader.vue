<template>
  <header class="header">
    <HeaderLinks />
    
    <template class="hidden md:flex">
      <HeaderNav />
    </template>
  </header>
</template>

<script setup lang="ts">
  import HeaderLinks from './HeaderLinks.vue';
  import HeaderNav from './HeaderNav.vue';
</script>

<style lang="scss">
  .header {
    @apply font-anybody flex w-full flex-col;
  }
</style>