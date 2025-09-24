<template>
  <div>
    <div class="about-section-area">
      <div class="heading1" id="services">
        <!-- <h5 data-aos="fade-left" data-aos-duration="800"><img :src="subLogo" alt="" />A propos</h5>
        <div class="space24" /> -->
        <h1 data-aos="fade-left" data-aos-duration="1000">Allier technique</h1>
        <div class="space24" />
        <h1 class="head" data-aos="fade-left" data-aos-duration="1100">
          avec <span>innovation</span>
        </h1>
      </div>
      <div class="space60" />
      <div class="about-boxarea">
        <BRow>
          <!-- <BCol lg="12" data-aos="fade-left" data-aos-duration="1200">
            <div class="about-main-boxes">
              <h4>Marcos MEDENOU</h4>
              <div class="space24" />
              <p>
                Bonjour, je suis Marcos MEDENOU, développeur logiciel spécialisé en Python, SaaS et Intelligence Artificielle. 
                Je crée des solutions digitales performantes et évolutives, 
                en transformant des problèmes complexes en systèmes simples et efficaces.
              </p>
            </div>
          </BCol> -->

          <BCol
            v-for="(item, idx) in skills"
            :key="idx"
            lg="6"
            md="6"
            data-aos="fade-up"
            data-aos-duration="1000"
            
          >
            <div class="about-boxes2">
              <img :src="item.image" alt="" />
              <div class="content-area">
                <h4>{{ item.title }}</h4>
                <div class="space16" />
                <p>{{ item.description }}</p>
              </div>
            </div>
          </BCol>

          <div class="space20" />

          <BCol lg="6" md="6" id="expériences">
            <h3>Expérience professionnelle</h3>
            <div class="space32" />
            <div class="about-others-box" data-aos="zoom-in" data-aos-duration="900">
              <a href="#">Janvier 2022 - Avril 2022</a>
              <div class="space16" />
              <h4><a href="#">Stagiaire Ingénierie Biomédicale</a></h4>
              <div class="space16" />
              <p>CHUD-Porto</p>
              <div class="space32" />
              <a href="#">Avril 2022 - Avril 2023</a>
              <div class="space16" />
              <h4><a href="#">Redacteur web SEO Freelance</a></h4>
              <div class="space16" />
              <p>Freelance</p>
              <div class="space32" />
              <a href="#">Avril 2023 - Décembre 2024</a>
              <div class="space16" />
              <h4><a href="#">Dévéloppeur web & mobile alternant </a></h4>
              <div class="space16" />
              <p>VIPP Digital Service</p>
              <div class="space32" />
              <a href="#">Janvier 2025 - Jusqu'a présent</a>
              <div class="space16" />
              <h4><a href="#">Coordonnateur de Projet logiciel</a></h4>
              <div class="space16" />
              <p>VIPP Digital Service</p>
            </div>
            <div class="about-others-box text-center" data-aos="zoom-in" data-aos-duration="1000">
              <h4>Stay With Me</h4>
              <div class="space18" />
              <ul>
                <li v-for="(item, idx) in socialLinks" :key="idx">
                  <a :href="item.url" :class="{ 'm-0': socialLinks.length - 1 === idx }">
                    <img :src="item.image" alt="" />
                  </a>
                </li>
              </ul>
            </div>
          </BCol>

          <BCol lg="6" md="6">
            <h3>Education</h3>
            <div class="space32" />
            <div class="about-others-box" data-aos="zoom-in" data-aos-duration="1100">
              <a href="#">Mai 2017 - Juin 2021</a>
              <div class="space16" />
              <h4><a href="#">Diplome de technicien biomédicale</a></h4>
              <div class="space16" />
              <p>Ecole Polytechique d'Abomey-Calavi</p>
              <div class="space32" />
              <a href="#">Juin 2022 - Juin 2024</a>
              <div class="space16" />
              <h4><a href="#">Diplome de Developpeur d'application web & mobile</a></h4>
              <div class="space16" />
              <p>HIGHFIVE UNIVERSITY</p>
              <div class="space32" />
              <a href="#">Juin 2024 - Decembre 2024</a>
              <div class="space16" />
              <h4><a href="#">Professional Foundations</a></h4>
              <div class="space16" />
              <p>ALX</p>
              <div class="space32" />
              <a href="#">Decembre 2024 - Mai 2025</a>
              <div class="space16" />
              <h4><a href="#">Diplome ProDev Back-End Developer</a></h4>
              <div class="space16" />
              <p>ALX</p>
            </div>
          </BCol>

          <div class="space20" />
        </BRow>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import subLogo from '@/assets/img/icons/sublogo1.svg'
import sIcon1 from '@/assets/img/icons/s-icon1.svg'
import sIcon2 from '@/assets/img/icons/s-icon2.svg'
import sIcon3 from '@/assets/img/icons/s-icon3.svg'
import sIcon4 from '@/assets/img/icons/s-icon4.svg'
import sIcon5 from '@/assets/img/icons/github3.svg'
import sIcon6 from '@/assets/img/icons/github2.svg'

import home2 from '@/assets/img/icons/home2.svg'
import home3 from '@/assets/img/icons/home3.svg'
import home4 from '@/assets/img/icons/home4.svg'
import home5 from '@/assets/img/icons/home5.svg'
import { BCol, BRow } from 'bootstrap-vue-next'

type SkillType = {
  image: string
  title: string
  description: string
}

const skills: SkillType[] = [
  {
    image: home2,
    title: 'Développement Backend',
    description:
      'Conception de systèmes robustes et évolutifs, garantissant des performances optimales et une architecture fiable.',
  },
  {
    image: home3,
    title: 'SaaS & Automatisation',
    description:
      'Création de plateformes SaaS intuitives et automatisées pour améliorer l’efficacité et simplifier les processus métier.',
  },
  {
    image: home4,
    title: 'IA & Analyse de Données',
    description:
      'Développement d’algorithmes IA performants pour transformer les données complexes en informations exploitables.',
  },
  {
    image: home5,
    title: 'Architecture & Optimisation',
    description:
      'Mise en place de structures logicielles claires et optimisées pour assurer maintenabilité et scalabilité.',
  },
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
</script>
