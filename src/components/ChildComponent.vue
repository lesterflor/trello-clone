<script setup lang="ts">
interface IItem {
  id: number
  name: string
}

defineProps<{ items: IItem[] }>()
</script>

<template>
  <ul>
    <li v-for="item in items" :key="item.id">
      <slot name="item" :item="item"></slot>
    </li>
  </ul>
</template>
