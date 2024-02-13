<template>
  <section class="links_wrapper">
    <nav class="header_links">
      <h4>
        <a href="/participate">Contribuisci</a>
      </h4>
      <h4>
        <a href="/subscribe">Abbonati</a>
      </h4>
    </nav>
    <article class="header_login">
        <IconProfile />
        <button>Accedi</button>
    </article>
  </section>
</template>

<script setup>
import IconProfile from '../icons/IconProfile.vue';

</script>

<style lang="scss">
  .links_wrapper {
    @apply w-full flex;
    @apply md:justify-between md:px-10 md:py-3;
  }

  .header {
    &_links {
      @apply w-full flex justify-around;
      @apply md:justify-start md:bottom-0;

       > * {
        @apply w-1/2 px-8 py-4 text-center border-y border-solid border-black text-sm;
        @apply md:border-0 md:p-0 md:w-fit;

        &:first-child {
          @apply border-r md:border-0 md:mr-6;
        }

        &:last-child {
          @apply border-l md:border-0;
        }
      }
    }

    &_login {
      @apply hidden md:flex md:text-sm;

      svg {
        @apply mr-1;
      }
    }
  }
</style>