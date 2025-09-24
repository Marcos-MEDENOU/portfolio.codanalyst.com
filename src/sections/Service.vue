<template>
  <div id="list-item-3">
    <div class="service-section-area">
      <BContainer>
        <BRow>
          <BCol lg="12">
            <div class="service-header heading1">
              <!-- <h5 data-aos="fade-left" data-aos-duration="800">
                <img :src="subLogo" alt="" />
                Mes Services
              </h5> -->
              <div class="space24" />
              <h2 data-aos="fade-left" data-aos-duration="1000">Solutions simple</h2>
              <div class="space24" />
              <h2 class="head" data-aos="fade-left" data-aos-duration="1100">
                Technologique <span>Fiable</span>
              </h2>
              <div class="space50" />

              <template v-for="(service, idx) in services" :key="idx">
                <div class="div" data-aos="fade-left" data-aos-duration="1000">
                  <div class="service-main-boxes">
                    <h4>{{ service.title }}</h4>
                    <div class="space24" />
                    <p>{{ service.description }}</p>
                  </div>
                </div>
                <div v-if="services.length - 1 !== idx" class="space30" />
              </template>
            </div>
          </BCol>
        </BRow>
      </BContainer>
    </div>
  </div>
</template>

<script setup lang="ts">
import subLogo from '@/assets/img/icons/sublogo1.svg'
import { BCol, BContainer, BRow } from 'bootstrap-vue-next'

type ServiceType = {
  title: string
  description: string
}

const services: ServiceType[] = [
  {
    title: 'Solutions Backend',
    description:
      'Conception de systèmes back-end robustes et évolutifs, garantissant performance et fiabilité.',
  },
  {
    title: 'Développement de plateformes SaaS',
    description:
      'Création de solutions SaaS intuitives et automatisées pour améliorer l’efficacité des entreprises.',
  },
  {
    title: 'Intelligence Artificielle & Analyse de Données',
    description:
      'Développement d’algorithmes IA performants pour transformer des données complexes en informations exploitables.',
  },
  {
    title: 'Architecture & Optimisation Logicielle',
    description:
      'Mise en place d’architectures claires et optimisées pour assurer scalabilité et maintenabilité des applications.',
  },
]
</script>
