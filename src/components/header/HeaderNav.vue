<template>
    <section class="navigation_wrapper">
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
    import type {KV} from '../../types/KeyValue';

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
    .navigation_wrapper {
      @apply w-full flex border-b border-solid border-black;
    }

    .header {
      &_navigation {
        @apply w-5/6 px-5;
        @apply xl:px-10;

        ul {
          > * {
            @apply flex justify-around font-raleway font-bold py-6 mr-4 text-center text-sm;
            @apply lg:text-lg lg:mr-4 lg:border-b-[9px] lg:border-white;
            @apply xl:text-2xl xl:mr-8;

            &:hover {
              @apply border-[#FF2C33] transition-colors;
            }

            &:last-child {
              @apply mr-0;
            }
          }
        }
      }
  
      &_switch {
        @apply flex w-1/6 items-center justify-center;
  
        > * {
          @apply p-1.5;

          &:last-child {
            @apply border border-solid border-black rounded shadow-[-2px_2px_0px_0px_#000000];

          }
        }

        svg {
          @apply w-6 h-6;
        }
      }
    }
  </style>