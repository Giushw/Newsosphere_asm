<template>
    <section class="anchors_wrapper">
      <nav class="footer_anchors">
        <ul>
          <li  v-for="anchor in anchors" :key="anchor.value">
            <a :href="`/${anchor.value}`">{{ anchor.label }}</a>
          </li>
        </ul>
      </nav>
      <section class="footer_copyright">
        <p>© 1994-2022 Newsosphere S.r.l.</p>
      </section>
    </section>
  </template>
  
  <script setup lang="ts">
    import { ref, type Ref } from 'vue';
    import type {KV} from '../../types/KeyValue';

    const anchors: Ref<KV[]> = ref([
      {
        label: 'Il Gruppo',
        value: 'group'
      },
      {
        label: 'Note Legali',
        value: 'legal'
      },
      {
        label: 'Chi Siamo',
        value: 'aboutus'
      },
      {
        label: 'Condizioni d\'uso',
        value: 'use'
      },
      {
        label: 'Privacy',
        value: 'privacy'
      },
      {
        label: 'Politica',
        value: 'politics'
      },
      {
        label: 'Scrivici',
        value: 'contactus'
      },
      {
        label: 'Pubblicità',
        value: 'ad'
      },
    ]);
  </script>
  
  <style lang="scss">
    .anchors_wrapper {
      @apply w-full flex flex-col px-4 py-6 border-t border-solid border-black bg-[#F4F4F4];
      @apply lg:flex-row lg:px-10 lg:py-12 lg:justify-between;
    }

    .footer {
      &_anchors {
        @apply w-1/2 mb-6;
        @apply lg:mb-0 lg:w-fit;

        ul {
          @apply flex flex-col;
          @apply lg:flex-row lg:items-center;

          > * {
            @apply text-base font-bold font-anybody flex justify-start pb-4;
            @apply lg:transition-colors lg:text-sm lg:font-normal lg:pb-0 lg:pr-6;

            &:hover {
              @apply md:text-[#FF2C33];
            }

            &:last-child {
              @apply p-0;
            }
          }
        }
      }
  
      &_copyright {
        @apply flex w-full items-center;
        @apply lg:w-fit lg:items-center lg:justify-end;

        p {
          @apply text-sm;
        }
      }
    }
  </style>