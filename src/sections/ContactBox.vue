<template>
  <div class="personal-contact-box">
    <div v-if="showMenu" class="list-group">
      <a
        v-for="(item, idx) in menuItems"
        :key="idx"
        class="list-group-item list-group-item-action"
        :class="{ active: activeSectionIndex === idx }"
        :href="'#' + item.url"
      >
        <img :src="item.image" alt="" />
        <span>{{ item.label }}</span>
    </a>
    </div>
    <div class="img1 image-anime">
      <img :src="heroImage" alt="" />
    </div>
    <div class="space18" />
    <h3>Marcos MEDENOU</h3>
    <div class="space16" />
    <p>
      Bonjour, je suis Marcos, un développeur logiciel passionné, spécialisé en Python et en IA, avec plusieurs années 
      d’expérience dans la création de solutions digitales performantes.
    </p>
    <div class="space32" />
    <ul>
      <li v-for="(item, idx) in socialLinks" :key="idx">
        <a :href="item.url" :class="{ 'm-0': socialLinks.length - 1 === idx }">
          <img :src="item.image" alt="" />
        </a>
      </li>
    </ul>
    <div class="space44" />
    <div class="btn-area1 text-center">
      <!-- <a href="#" download class="vl-btn1">
        Télécharger mon CV
        <img :src="downloadIcon" alt="" />
      </a> -->
    </div>
    <!-- <div class="space16" /> -->
    <!-- <div class="space32" /> -->
    <p>© {{ currentYear }} {{ appName }}. Tous droits réservés.</p>
  </div>
</template>

<script setup lang="ts">
import home1 from '@/assets/img/icons/home1.svg'
import home2 from '@/assets/img/icons/home2.svg'
import home3 from '@/assets/img/icons/home3.svg'
import home4 from '@/assets/img/icons/home4.svg'
import home5 from '@/assets/img/icons/home5.svg'
import home6 from '@/assets/img/icons/home6.svg'
import home7 from '@/assets/img/icons/home7.svg'
import home8 from '@/assets/img/icons/home8.svg'

import heroImage from '@/assets/img/all-images/hero/HERO-IMG.jpg'
import downloadIcon from '@/assets/img/icons/download1.svg'

import sIcon1 from '@/assets/img/icons/s-icon1.svg'
import sIcon2 from '@/assets/img/icons/s-icon2.svg'
import sIcon3 from '@/assets/img/icons/s-icon3.svg'
import sIcon4 from '@/assets/img/icons/s-icon4.svg'
import sIcon5 from '@/assets/img/icons/github.svg'

import { appName, currentYear } from '@/helpers'
import { onMounted, ref } from 'vue'

type PropsType = {
  showMenu?: boolean
}

const props = withDefaults(defineProps<PropsType>(), {
  showMenu: true,
})

type MenuItemType = {
  label: string
  url: string
  image: string
}

const menuItems: MenuItemType[] = [
  { label: 'Accueil', url: 'accueil', image: home1 },
  { label: 'Services', url: 'services', image: home2 },
  { label: 'Expériences', url: 'expériences', image: home3 },
  { label: 'Compétences', url: 'compétences', image: home4 },
  { label: 'Portfolio', url: 'portfolio', image: home5 }
  // { label: 'Testimonial', url: 'list-item-6', image: home6 },
  // { label: 'Blog', url: 'list-item-7', image: home8 },
  // { label: 'Contactez', url: 'list-item-8', image: home7 }, 
]

type SocialLinkType = {
  label?: string
  image: string
  url: string
}

const socialLinks: SocialLinkType[] = [
  { image: sIcon1, url: 'https://twitter.com/MMedenou86706' },
  { image: sIcon2, url: 'https://www.instagram.com/mmedenou/' },
  { image: sIcon3, url: 'https://www.facebook.com/marcos.freeman.9' },
  { image: sIcon4, url: 'https://www.linkedin.com/in/marcos-medenou-1b574b303' },
  // { image: sIcon5, url: 'https://github.com/Marcos-MEDENOU' },
]

onMounted(() => {
  if (props.showMenu) window.addEventListener('scroll', getActiveSectionIndex)
})

const activeSectionIndex = ref<number>(0)

const getActiveSectionIndex = () => {
  const currentScrollPos = window.pageYOffset

  for (let i = 0; i < menuItems.length; i++) {
    const section = document.getElementById(menuItems[i].url)

    if (section) {
      const sectionTop = section.offsetTop - 70
      const sectionHeight = section.offsetHeight
      if (currentScrollPos >= sectionTop && currentScrollPos < sectionTop + sectionHeight) {
        activeSectionIndex.value = i
        break
      }
    }
  }
}
</script>
