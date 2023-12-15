<style lang="sass" scoped>
.picture
  -webkit-filter: brightness(105%) hue-rotate(350deg) sepia(10%)
  filter: brightness(105%) hue-rotate(350deg) sepia(10%)

.firstname
  font-size: 4em

.lastname
  font-size: 10em
</style>

<template>
  <q-page>
    <div class="row justify-center items-center window-height justify-around">
      <div class="row">
        <span class="firstname">John Louie</span>
        <span class="lastname text-weight-bolder text-secondary">Hiyas</span>
      </div>
      <img class="picture" src="~assets/picture.png" />
    </div>

    <AboutComponent class="animated bounce"/>
    <ServiceComponent class="animated bounce"/>
    <ContactComponent class="animated bounce"/>
  </q-page>
</template>

<script setup>
import { defineComponent } from 'vue'
import AboutComponent from 'components/AboutComponent.vue';
import ServiceComponent from 'components/ServiceComponent.vue';
import ContactComponent from 'components/ContactComponent.vue';

defineComponent({
  name: 'IndexPage'
})
</script>
