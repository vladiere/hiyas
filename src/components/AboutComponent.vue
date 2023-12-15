<template>
  <div :class="Platform.is.mobile ? 'column q-px-md text-center justify-center bg-dark text-white q-pb-xl' : 'window-height column q-px-xl justify-center bg-dark text-white'">
    <div class="q-pt-md text-h1 row q-mb-xl q-gutter-x-xs text-weight-bolder">
      <span>About</span>
      <span class="text-secondary">Me</span>
    </div>
    <span class="text-h3 text-weight-regular">John Louie Hiyas</span>
    <span class="text-h6 text-weight-light">As a front-end web developer, I thrive on transforming creative visions into engaging digital experiences. With a keen eye for design and proficiency in cutting-edge technologies, I craft visually stunning and user-friendly interfaces that elevate the online presence of businesses and individuals alike</span>
  </div>
</template>

<script setup>
import { Platform } from 'quasar';
</script>
