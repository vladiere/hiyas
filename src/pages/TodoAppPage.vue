<template>
  <q-page padding class="column items-center">
    <div class="column q-gutter-y-md" :style="Platform.is.mobile ? 'width: 90%' : 'width: 30%'">
      <div class="row justify-between">
        <q-btn label="home" to="/" color="secondary"/>
      </div>
      <q-input v-model="newList" @keyup.enter="addNewList" outlined label="Add new list" dense />
      <q-list bordered separator v-if="lists.length !== 0">

        <q-item v-ripple v-for="(item, index) in lists" :key="index">
          <q-item-section>
            <q-item-label :class="item.status === 'done' ? 'text-capitalize text-strike text-italic text-grey-7' : 'text-capitalize'">{{ item.todo }}</q-item-label>
          </q-item-section>
          <q-item-section side>
            <div class="row q-gutter-x-md">
              <q-icon name="mdi-check-all" color="positive" class="cursor-pointer col" size="2em" @click="item.status === 'not' ? item.status = 'done' : item.status = 'not'"/>
              <q-icon name="mdi-trash-can" color="negative" class="cursor-pointer col" size="2em" @click="lists.splice(index,1)"/>
            </div>
          </q-item-section>
        </q-item>

      </q-list>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue';
import { Platform, uid } from 'quasar';

const newList = ref('');
const lists = ref([]);

const addNewList = () => {
  if (newList.value) {
    lists.value.push({
      id: uid(),
      todo: newList.value,
      status: 'not',
    });

    newList.value = '';
  }
}
</script>
