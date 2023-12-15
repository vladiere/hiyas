<template>
  <q-page padding class="column items-center">
    <div class="column q-gutter-y-md" :style="Platform.is.mobile ? 'width: 90%' : 'width: 30%'">
      <div class="row justify-between">
        <q-btn label="home" to="/" color="secondary"/>
        <q-btn label="restart" color="primary" @click="restartGame" />
      </div>
      <q-input :disable="isGuessed" @keyup.enter="guessTheNumber" v-model="word" outlined label="Enter your guess number (1 to 100)" type="number" min="0"/>

      <div class="column text-center" v-if="isGuessed">
        <span class="text-h6 text-weight-light">{{ message }}</span>
        <span class="text-h1">{{ randomNumber }}</span>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue';
import { Platform } from 'quasar';

const word = ref(null);
const randomNumber = ref(Math.floor(Math.random() * 100));
const isGuessed = ref(false);
const message = ref('')

const guessTheNumber  = () => {
  console.log(randomNumber.value)
  isGuessed.value = true;
  if (randomNumber.value === word.value) {
    message.value = 'Nice! you got it right';
  } else {
    message.value = 'To bad you did not guess it right!';
  }
}

const restartGame = () => {
  randomNumber.value = null;
  word.value = null;
  isGuessed.value = false;
  randomNumber.value = ref(Math.floor(Math.random() * 100));
}
</script>
