<template>
  <section class="tba_wrapper">
    <article class="tba_content">
      <span>503</span>
      <h1>Sito in costruzione</h1>
      <p>Siamo spiacenti, il sito è ancora in fase di lavorazione e arriverà al più presto.</p>
    </article>
  </section>
</template>

<script setup lang="ts">

</script>

<style lang="scss">
  .tba {
    &_wrapper {
      @apply grid min-h-full place-items-center bg-[#F4F1DE] px-6 py-24;
      @apply sm:py-32;
      @apply lg:px-8;
    }

    &_content {
      @apply text-center;

      span {
        @apply font-raleway font-semibold text-[#FF2C33];
      }

      h1 {
        @apply font-anybody mt-4 text-3xl font-bold tracking-tight text-black sm:text-5xl;
      }
      
      p {
        @apply font-raleway mt-6 text-base leading-7 text-gray-600;
      }
    }
  }
</style>