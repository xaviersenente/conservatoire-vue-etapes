<script setup lang="ts">
import DuotoneImg from '@/components/DuotoneImg.vue'
import { formatDate } from '@/helper'

const props = defineProps<{
  id: number
  title: string
  date: string
  excerpt: string
  imgCardPath: string
  imgAlt?: string
}>()

const url = `/events/${props.id}`
</script>

<template>
  <article
    class="group col-span-4 grid grid-cols-[24px_1fr] grid-rows-[200px_48px_1fr] lg:grid-cols-[2fr_11fr]"
  >
    <DuotoneImg
      :imgPath="imgCardPath"
      :imgAlt="imgAlt"
      classPicture="group-hover:before:bg-black col-start-1 row-start-1 col-span-2 row-span-2"
      classImg="group-hover:grayscale-0 group-hover:mix-blend-normal"
    />
    <h3 class="z-[1] col-start-2 row-start-1 my-6 mr-4 self-end font-serif text-3xl text-white">
      <a :href="`${url}`">{{ title }}</a>
    </h3>
    <div class="z-[2] col-span-1 col-start-2 row-span-2 row-start-2 space-y-4 bg-white p-6">
      <p class="uppercase">{{ formatDate(date) }}</p>
      <p>{{ excerpt }}</p>
      <a class="inline-block border-b-2 border-black uppercase" :href="`${url}`">Plus d'info</a>
    </div>
  </article>
</template>
