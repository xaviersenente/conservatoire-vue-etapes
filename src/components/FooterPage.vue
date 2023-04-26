<script setup lang="ts">
import FacebookIcon from '@/components/icons/IconFacebook.vue'
import TwitterIcon from '@/components/icons/IconTwitter.vue'
import YoutubeIcon from '@/components/icons/IconYoutube.vue'
import InstagramIcon from '@/components/icons/IconInstagram.vue'
import LogoGBIcon from '@/components/icons/IconLogoGB.vue'
import LogoFooterIcon from '@/components/icons/IconLogoFooter.vue'
</script>

<template>
  <footer class="grille space-y-6 bg-gray-900 py-16 px-6 text-white lg:space-y-0">
    <LogoFooterIcon />

    <nav class="col-span-3 col-start-7 space-y-3">
      <h4 class="font-bold uppercase">Menu</h4>
      <ul>
        <li><a href="#">Mentions légales</a></li>
        <li><a href="#">Archives</a></li>
        <li><a href="#">Contact et accès</a></li>
      </ul>
    </nav>

    <div class="col-span-3 col-start-10 space-y-3">
      <h4 class="font-bold uppercase">Contact</h4>
      <address>
        1 rue Paul Koepfler<br />90000 Belfort<br />
        <a href="tel:0384542727">03 84 54 27 27</a><br />
        <a href="mailto:conservatoire@agglo-belfort.fr">conservatoire@agglo-belfort.fr</a>
      </address>
    </div>

    <div class="col-span-3 col-start-7">
      <LogoGBIcon />
    </div>

    <div class="col-span-3 col-start-10 space-y-3">
      <h4 class="font-bold uppercase">Nous suivre</h4>
      <ul class="flex gap-4">
        <li>
          <a href="https://facebook.com" aria-label="facebook">
            <FacebookIcon />
          </a>
        </li>
        <li>
          <a href="https://instagram.com" aria-label="instagram">
            <TwitterIcon />
          </a>
        </li>
        <li>
          <a href="https://twitter.com" aria-label="twitter">
            <YoutubeIcon />
          </a>
        </li>
        <li>
          <a href="https://youtube.com" aria-label="youtube">
            <InstagramIcon />
          </a>
        </li>
      </ul>
    </div>
  </footer>
</template>
