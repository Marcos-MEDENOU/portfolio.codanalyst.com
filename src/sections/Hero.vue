<template>
  <div id="list-item-1">
    <div class="hero-heading-area heading1">
      <div class="space24" />
      <!-- <h5 data-aos="fade-left" data-aos-duration="800">
        <img :src="subLogo" alt="" />Salut👋, je suis Marcos, Analyste Programmeur
      </h5> -->
   
      <h1 data-aos="fade-left" data-aos-duration="900">Développeur Backend</h1>
      <div class="space24" />
      <h1 class="head" data-aos="fade-left" data-aos-duration="1000">
        Certifié <span>ProDev ALX</span>
      </h1>
      <div class="space24" />
      <!-- <p data-aos="fade-left" data-aos-duration="1100">
        Votre passerelle vers des solutions innovantes, des expériences fluides et des résultats percutants. Je transforme des idées complexes en solutions simples et accessibles.
      </p> -->
      <div class="space24" />
      <BCol lg="12" data-aos="fade-left" data-aos-duration="1100">
            <div class="portfolio-boxarea click-here">
              <div class="img1">
                <a href="javascript:void(0)">
                  <img :src="alxCertificate" alt="" />
                </a>
              </div>
              <div class="space24" />
             
            </div>
          </BCol>
      <div class="space32" />
      <div class="main-btn-area" data-aos="fade-up" data-aos-duration="1200">
        <a href="https://savanna.alxafrica.com/certificates/R9EfSXNsm7" target="_blank"
          >Vérifier l'authenticité du certificat 🚀
          <span class="icon">
            <Icon icon="fa6-solid:arrow-right" />
          </span>
        </a>
      </div>
    </div> 
  </div>
</template>

<script setup lang="ts">
import subLogo from '@/assets/img/icons/sublogo1.svg'
import elements1 from '@/assets/img/elements/elements1.png'
import arrow1 from '@/assets/img/icons/arrow1.svg'
import others1 from '@/assets/img/all-images/others/others1.png'
import { Icon } from '@iconify/vue'
import alxCertificate from '@/assets/img/all-images/portfolio/86-prodev-backend-certificate-marcos-medenou.png'
</script>
