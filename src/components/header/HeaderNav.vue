<template>
    <section class="w-full flex">
      <nav class="header_navigation">
        <ul class="flex">
          <li  v-for="section in sections" :key="section.value">
            <a :href="`/${section.value}`">{{ section.label }}</a>
          </li>
        </ul>
      </nav>
      <section class="header_switch">
        <picture>
          <IconAa />
        </picture>
        <picture>
          <IconVector />
        </picture>
      </section>
    </section>
  </template>
  
  <script setup lang="ts">
    import { ref, type Ref } from 'vue';
    import IconAa from '../icons/IconAa.vue';
    import IconVector from '../icons/IconVector.vue';

    interface KV {
      label: string,
      value: string
    };

    const sections: Ref<KV[]> = ref([
      {
        label: 'Tutti i Temi',
        value: 'allthemes'
      },
      {
        label: 'Ambiente',
        value: 'environment'
      },
      {
        label: 'Economia',
        value: 'economy'
      },
      {
        label: 'Mondo',
        value: 'world'
      },
      {
        label: 'Non Profit',
        value: 'noprofit'
      },
      {
        label: 'Politica',
        value: 'politics'
      },
      {
        label: 'Società',
        value: 'society'
      },
      {
        label: 'Welfare',
        value: 'welfare'
      },
    ]);
  </script>
  
  <style lang="scss">
    .header {
      &_navigation {
        @apply w-5/6 px-6 border-b;

        ul {
          > * {
            @apply flex justify-around font-raleway font-bold px-4 py-6 text-center text-xl border-b-4 border-white;
            @apply lg:text-2xl;

            &:hover {
              @apply border-red-500 transition-colors;
            }
          }
        }
      }
  
      &_switch {
        @apply flex w-1/6 items-center justify-center;
  
        > * {
          @apply p-1.5;

          &:last-child {
            @apply border border-solid rounded shadow-[-2px_2px_0px_0px_#000000];

          }
        }

        svg {
          @apply w-6 h-6;
        }
      }
    }
  
  
  </style>