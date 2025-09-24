<template>
  <div id="portfolio">
    <div class="portfolio-section-area">
      <BContainer>
        <BRow>
          <BCol lg="12">
            <div class="portfolio-header heading1">
              <!-- <h5 data-aos="fade-left" data-aos-duration="800">
                <img :src="subLogo" alt="" />
                Mes réalisations
              </h5> -->
              <div class="space24" />
              <h2 data-aos="fade-left" data-aos-duration="1000">Collaborations Réels</h2>
              <div class="space24" />
              <h2 class="head" data-aos="fade-left" data-aos-duration="1100">
                Réel <span>Resultats</span>
              </h2>
            </div>
          </BCol>
          <div class="space50" />
          <BCol lg="12" data-aos="fade-left" data-aos-duration="1000">
            <div class="portfolio-boxarea click-here">
              <div class="img1">
                <a href="https://alx-project-nexus-marcos.vercel.app/swagger/">
                  <img :src="portfolio1" alt="" />
                </a>
                <!-- <a href="javascript:void(0)" @click="openModal">
                  <img :src="portfolio1" alt="" />
                </a> -->
              </div>
              <div class="space24" />
              <a href="https://alx-project-nexus-marcos.vercel.app/swagger/"
                >Scalable Ecommerce API (alx nexus)</a
              >
              <!-- <a href="javascript:void(0)" @click="openModal"
                >Scalable Ecommerce API (alx nexus)</a
              > -->
            </div>
          </BCol>

          <BCol lg="6" md="6" data-aos="fade-left" data-aos-duration="1100">
            <div class="portfolio-boxarea2 click-here">
              <div class="img1">
                <a href="javascript:void(0)">
                  <img :src="portfolio3" alt="" />
                </a>
              </div>
              <div class="space24" />
              <a href="javascript:void(0)">Formulaire d'enregistrement des données 
                de collecte dans une base de donnée externe</a>
            </div>
          </BCol>

          <BCol lg="6" md="6" data-aos="fade-left" data-aos-duration="1200">
            <div class="portfolio-boxarea2 click-here">
              <div class="img1">
                <a href="javascript:void(0)">
                  <img :src="portfolio4" alt="" />
                </a>
              </div>
              <div class="space24" />
              <a href="javascript:void(0)">Espace vendeur</a>
            </div>
          </BCol>

          <BCol lg="12" data-aos="fade-left" data-aos-duration="1100">
            <div class="portfolio-boxarea click-here">
              <div class="img1">
                <a href="javascript:void(0)">
                  <img :src="portfolio2" alt="" />
                </a>
              </div>
              <div class="space24" />
              <a href="javascript:void(0)"
                >Espace admin pour une application de gestion de produits agricoles</a
              >
            </div>
          </BCol>
        </BRow>
      </BContainer>
    </div>
  </div>

  <ContactModal v-model="showModal" />
</template>

<script setup lang="ts">
import subLogo from '@/assets/img/icons/sublogo1.svg'

import portfolio1 from '@/assets/img/all-images/portfolio/alx-nexus.png'
import portfolio2 from '@/assets/img/all-images/portfolio/agriconnect.png'
import portfolio3 from '@/assets/img/all-images/portfolio/portfolio6.png'
import portfolio4 from '@/assets/img/all-images/portfolio/portfolio7.png'
import ContactModal from '@/components/ContactModal.vue'
import { ref } from 'vue'
import { BCol, BContainer, BRow } from 'bootstrap-vue-next'

const showModal = ref<boolean>(false)

const openModal = () => (showModal.value = true)
</script>
