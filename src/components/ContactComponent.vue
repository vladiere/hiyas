<template>
  <div :class="Platform.is.mobile ? 'column justify-center bg-secondary q-py-xl' : 'window-height column justify-center bg-secondary'">
    <div :class="Platform.is.mobile ? 'column q-px-md' : 'row q-gutter-x-lg q-mx-xl'">
      <div :class="Platform.is.mobile ? 'column q-gutter-y-lg' : 'col column q-gutter-y-lg'">
        <span :class="Platform.is.mobile ? 'text-h2 text-weight-bolder' : 'text-h1 text-weight-bolder'">CONTACT</span>
        <div class="column q-gutter-y-sm">
          <span class="text-h4 text-capitalize text-weight-bolder">you got a problem to solve?</span>
          <span class="text-h6 text-weight-light">Get your engine start and tell me what's you idea and i'll turn it into application</span>
          <span class="text-h6 text-weight-regular row items-center"><q-icon size="1.5em" name="mdi-email-outline" />johnlouiehiyas@gmail.com</span>
        </div>
      </div>
      <div class="col column q-gutter-y-sm">
        <div class="column">
          <span class="text-h6">Name:</span>
          <q-input outlined />
        </div>
        <div class="column q-gutter-y-xs">
          <span class="text-h6">Email:</span>
          <q-input outlined />
        </div>
        <div class="column q-gutter-y-xs">
          <span class="text-h6">Message:</span>
          <q-input outlined type="textarea"/>
        </div>
        <q-btn class="self-start" outline label="hit me up" icon-right="mdi-send" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { Platform } from 'quasar';
</script>
