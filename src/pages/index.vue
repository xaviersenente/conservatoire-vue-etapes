<script setup lang="ts">
import Hero from '@/components/Hero.vue'
import IconTheater from '@/components/icons/IconTheater.vue'
import IconMusic from '@/components/icons/IconMusic.vue'
import IconDanse from '@/components/icons/IconDanse.vue'
</script>
<template>
  <Hero
    title="Conservatoire Henri Dutilleux"
    subTitle="Conservatoire à Rayonnement Départemental du Grand Belfort"
    imgPath="./img/crd-int-01.webp"
    imgAlt="Photo de l'entrée du Conservatoire Henri Dutilleux"
  >
    <template #chapo>
      <nav class="flex-1 font-serif lg:text-3xl">
        <ul class="grid grid-cols-3 gap-12">
          <li>
            <a class="flex flex-col items-center gap-4 lg:flex-row" href="#">
              <IconMusic /> Musique
            </a>
          </li>
          <li>
            <a class="flex flex-col items-center gap-4 lg:flex-row" href="#">
              <IconTheater /> Théâtre
            </a>
          </li>
          <li>
            <a class="flex flex-col items-center gap-4 lg:flex-row" href="#">
              <IconDanse /> Danse
            </a>
          </li>
        </ul>
      </nav>
    </template>
  </Hero>
</template>
