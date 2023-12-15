<template>
  <div :class="Platform.is.mobile ? 'column justify-center q-py-xl' : 'window-height column justify-center'">
    <div :class="Platform.is.mobile ? 'column' : 'row q-mx-md items-center'">
      <img :class="Platform.is.mobile ? '' : 'col'" :style="Platform.is.mobile ? 'width: 100%' : ''" src="~assets/work.png" />
      <div :class="Platform.is.mobile ? 'column q-gutter-y-xl' : 'col-6 column q-gutter-y-xl q-px-xl'">
        <span class="text-h1 text-weight-bolder">WORK</span>

        <div :class="Platform.is.mobile ? 'q-ml-md column' : 'q-ml-xl column'">
          <span class="text-h6">Todo List App</span>
          <span class="text-subtitle1">A minimal todo list application using VUEjs</span>
          <q-btn outline color="secondary" class="self-start" padding="2px 25px" label="explore" to="/todo_list"/>
        </div>

        <div :class="Platform.is.mobile ? 'q-ml-md column' : 'q-ml-xl column'">
          <span class="text-h6">Simple Guessing Game App</span>
          <span class="text-subtitle1">A simple number guessing game powered by VUEjs</span>
          <q-btn outline color="secondary" class="self-start" padding="2px 25px" label="explore" to="/guess_game" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Platform } from 'quasar';
</script>
