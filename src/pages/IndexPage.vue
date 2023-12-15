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
    <div :class="Platform.is.mobile ? 'window-height column justify-center text-center q-pt-lg' : 'row justify-center items-center window-height justify-around'">
      <div :class="Platform.is.mobile ? 'column' : 'row'">
        <span :class="Platform.is.mobile ? 'text-h3' : 'firstname'">John Louie</span>
        <span :class="Platform.is.mobile ? 'text-weight-bolder text-secondary text-h1' : 'lastname text-weight-bolder text-secondary'">Hiyas</span>
      </div>
      <img class="picture self-end" src="~assets/picture.png" :style="Platform.is.mobile ? 'width: 100%' : ''" />
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
import { Platform } from 'quasar';

defineComponent({
  name: 'IndexPage'
})
</script>
