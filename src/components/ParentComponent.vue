<script setup lang="ts">
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const items = ref([
  {
    id: 1,
    name: 'item 1',
  },
  {
    id: 2,
    name: 'item 2',
  },
  {
    id: 3,
    name: 'item 3',
  },
])
</script>

<template>
  <div>
    <h1>Item list</h1>
    <ChildComponent :items="items">
      <template #item="{ item }">
        <strong class="text-2xl">{{ item.name }}</strong>
      </template>
    </ChildComponent>
  </div>
</template>
