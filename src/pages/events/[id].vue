<script setup lang="ts">
import { events } from '@/data'
import DuotoneImg from '@/components/DuotoneImg.vue'
import { formatDate } from '@/helper'
import Patterns from '@/components/icons/Patterns.vue'
import { animateLines } from '@/helper'
animateLines()

const props = defineProps<{ id: string }>()
const event = events.find((event) => event.id === Number(props.id))
</script>
<template>
  <div v-if="event">
    <div class="grille relative pt-28 lg:grid">
      <DuotoneImg :imgPath="event.imgPath" :imgAlt="event.imgAlt" classPicture="col-span-5" />
      <header class="col-span-6 col-start-7">
        <h1 class="my-12">{{ event.title }}</h1>
        <ul class="divide-y">
          <li class="grid grid-cols-4 items-center py-4">
            <span class="col-span-1 text-sm font-bold uppercase">Date</span>
            <span class="col-span-3">{{ formatDate(event.date) }}</span>
          </li>
          <li class="grid grid-cols-4 items-center py-4">
            <span class="col-span-1 text-sm font-bold uppercase">Lieux</span>
            <span class="col-span-3">{{ event.lieu }}</span>
          </li>
          <li class="grid grid-cols-4 items-center py-4">
            <span class="col-span-1 text-sm font-bold uppercase">Catégorie</span>
            <span class="col-span-3">{{ event.categorie }}</span>
          </li>
        </ul>
      </header>
    </div>
    <div
      class="absolute inset-0 z-[-1] flex items-center justify-end overflow-hidden stroke-pink stroke-[24px] opacity-40"
    >
      <Patterns class="-ml-60 -mr-[5vw] lg:ml-auto" />
    </div>
    <p class="mx-auto my-12 max-w-4xl px-6 text-2xl leading-normal lg:text-3xl lg:leading-relaxed">
      {{ event?.excerpt }}
    </p>
    <div class="mx-auto my-12 max-w-2xl space-y-3 px-6" v-html="event?.description"></div>
  </div>
  <div v-else>
    <h1>Pas d'événement correspondant</h1>
  </div>
</template>
