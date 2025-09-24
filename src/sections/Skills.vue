<template>
  <div >
    <div class="skill-section-area" id="compétences">
      <BContainer>
        <BRow>
          <BCol lg="12">
            <div class="skill-header heading1">
              <!-- <h5 data-aos="fade-left" data-aos-duration="800">
                <img :src="subLogo" alt="" />
                Mes Compétences
              </h5> -->
              <div class="space24" />
              <!-- <h2 data-aos="fade-left" data-aos-duration="1000">The Tools Behind</h2> -->
              <div class="space24" />
              <h2 class="head" data-aos="fade-left" data-aos-duration="1100">
                Outils et <span>Technologies</span>
              </h2>
            </div>
            <div class="space80" />
            <BRow>
              <BCol
                v-for="(item, idx) in skills"
                :key="idx"
                lg="4"
                md="6"
                data-aos="zoom-out"
                data-aos-duration="1000"
              >
                <div class="skill-boxarea">
                  <div class="icons">
                    <img :src="item.image" alt="" />
                  </div>
                  <div class="space24" />
                  <h3>
                    <count-up
                      :end-val="item.percentage"
                      :options="{ suffix: '%' }"
                      class="counter"
                    />
                  </h3>
                  <div class="space16" />
                  <p>{{ item.title }}</p>
                </div>
              </BCol>
            </BRow>
          </BCol>
        </BRow>
      </BContainer>
    </div>
  </div>
</template>

<script setup lang="ts">
import subLogo from '@/assets/img/icons/sublogo1.svg'
import skill1 from '@/assets/img/icons/skill1.svg'
import skill2 from '@/assets/img/icons/skill2.svg'
import skill3 from '@/assets/img/icons/skill3.svg'
import skill4 from '@/assets/img/icons/skill4.svg'
import skill5 from '@/assets/img/icons/skill5.svg'
import skill6 from '@/assets/img/icons/skill6.svg'
import nodejs from '@/assets/img/icons/nodejs.svg'
import react from '@/assets/img/icons/react.svg'
import django from '@/assets/img/icons/django.svg'
import fastapi from '@/assets/img/icons/fastapi.svg'
import github from '@/assets/img/icons/github.svg'
import nginx from '@/assets/img/icons/nginx.svg'
import postgresql from '@/assets/img/icons/postgresql.svg'
import sql from '@/assets/img/icons/mysql2.svg'
import wordpress from '@/assets/img/icons/wordpress.svg'

import CountUp from 'vue-countup-v3'
import { BCol, BContainer, BRow } from 'bootstrap-vue-next'

type SkillType = {
  title: string
  percentage: number
  image: string
}

const skills: SkillType[] = [
  {
    title: 'Django',
    percentage: 95,
    image: django,
  },
  {
    title: 'FastAPI',
    percentage: 87,
    image: fastapi,
  },
  {
    title: 'React',
    percentage: 82,
    image: react,
  },

  {
    title: 'NodeJS',
    percentage: 78,
    image: nodejs,
  },
  {
    title: 'Github',
    percentage: 80,
    image: github,
  },
  {
    title: 'NGINX',
    percentage: 78,
    image: nginx,
  },
  {
    title: 'POSTGRESQL',
    percentage: 74,
    image: postgresql,
  },
  {
    title: 'SQL',
    percentage: 84,
    image: sql,
  },
  {
    title: 'Wordpress',
    percentage: 85,
    image: wordpress,
  },
]
</script>
