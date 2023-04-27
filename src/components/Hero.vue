<script setup lang="ts">
import DuotoneImg from '@/components/DuotoneImg.vue'

defineProps<{
  title: string
  imgPath: string
  imgAlt: string
  subTitle?: string
}>()
</script>
<template>
  <div class="grille relative grid h-screen grid-rows-[4fr_1fr] lg:grid-rows-[3fr_1fr]">
    <div class="col-span-9 my-12 space-y-8 self-end text-white">
      <h1>{{ title }}</h1>
      <h2 v-if="subTitle" class="font-sans text-sm font-bold uppercase">
        {{ subTitle }}
      </h2>
    </div>

    <div
      class="relative col-span-9 row-start-2 -mx-6 flex items-center bg-white px-6 lg:mx-0 lg:pl-0 lg:before:absolute lg:before:top-0 lg:before:ml-[-100%] lg:before:h-full lg:before:w-full lg:before:bg-white"
    >
      <slot name="chapo"></slot>
    </div>
    <DuotoneImg
      :imgPath="imgPath"
      :imgAlt="imgAlt"
      classPicture="!absolute inset-0 object-cover z-[-1]"
    />
    <slot name="patterns"></slot>
  </div>
</template>
