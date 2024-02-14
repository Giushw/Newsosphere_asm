<template>
  <section class="searchMenu_wrapper">
    <article class="header_menu">
      <picture>
        <IconMenu />
      </picture>
    </article>
    <article class="header_logo">
      <picture>
        <LogoFull />
      </picture>
    </article>
    <article class="header_search">
      <picture>
        <IconSearch />
      </picture>
    </article>
  </section>
</template>
  
<script setup lang="ts">
  import IconMenu from '../icons/IconMenu.vue';
  import IconSearch from '../icons/IconSearch.vue';
  import LogoFull from '../illustrations/LogoFull.vue';
</script>
  
  <style lang="scss">
    .searchMenu_wrapper {
      @apply font-anybody flex w-full border-y border-solid border-black;
      @apply md:max-h-[96px];
    }

    .header {
      &_menu {
        @apply w-1/4;
        @apply md:max-w-[96px];

        picture {
          @apply w-full h-full p-4 flex justify-center items-center;
          @apply  md:p-9;
        }

        svg {
          @apply w-5 h-5;
          @apply md:w-6 h-6;
        }
      }

      &_logo {
        @apply w-2/4 border-x border-solid border-black;
        @apply md:w-full;

        picture {
          @apply w-full h-full p-4 flex justify-center items-center;
          @apply  md:p-8;

          svg {
            @apply w-full h-full;
          }
        }
      }

      &_search {
        @apply w-1/4;
        @apply md:max-w-[96px];

        picture {
          @apply  w-full h-full p-4 flex justify-center items-center;
          @apply  md:p-9;

          svg {
            @apply w-5 h-5;
            @apply md:w-6 h-6;
          }
        }
      }
    }
  </style>