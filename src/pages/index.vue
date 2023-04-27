<script setup lang="ts">
import Hero from '@/components/Hero.vue'
import IconTheater from '@/components/icons/IconTheater.vue'
import IconMusic from '@/components/icons/IconMusic.vue'
import IconDanse from '@/components/icons/IconDanse.vue'
import Button from '@/components/Button.vue'
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
  <section class="grille my-24 grid-rows-2 space-y-8 lg:space-y-0">
    <div class="col-span-7 col-start-1 row-span-2 row-start-1">
      <img src="/img/crd-int-01.webp" alt="Salle de musique du conservatoire" />
    </div>
    <header class="col-span-7 col-start-6 row-span-1 row-start-1 space-y-8 bg-white lg:p-16">
      <h2 class="text-xl italic leading-normal lg:text-3xl">
        Découvrez le Conservatoire, ses enseignements, ses équipes dans un nouveau lieu dédié à la
        culture artistique.
      </h2>
      <Button url="/conservatoire" text="Plus d'info" />
    </header>

    <div class="col-span-4 col-start-9 row-start-2 grid grid-cols-2 gap-12">
      <p>
        <span class="block text-4xl text-pink lg:text-6xl">9</span>
        <span>sites</span>
      </p>
      <p>
        <span class="block text-4xl text-pink lg:text-6xl">84</span>
        <span>enseignants</span>
      </p>
      <p>
        <span class="block text-4xl text-pink lg:text-6xl">1500</span>
        <span>élèves</span>
      </p>
      <p>
        <span class="block text-4xl text-pink lg:text-6xl">50</span>
        <span>disciplines</span>
      </p>
    </div>
  </section>
</template>
