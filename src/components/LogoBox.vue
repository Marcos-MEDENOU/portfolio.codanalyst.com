<template>
  <div class="site-logo" :class="className">
    <RouterLink to="/" class="hero-heading-area heading1">
      
      <!-- <img :src="logo" alt="" :width="width" :height="height" /> -->
      <!-- <h1 class="head" data-aos="fade-left" data-aos-duration="1000">
         <span>Codanalyst</span>
      </h1> -->
    </RouterLink>
  </div>
</template>

<script setup lang="ts">
import logo from '@/assets/img/logo/LOGO.png'

type PropsType = {
  height?: number
  width?: string
  className?: string
}

defineProps<PropsType>()
</script>
