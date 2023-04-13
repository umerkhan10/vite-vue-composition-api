<template>
  <p class="text-left ml-8 text-slate-400 font-bold">What are you looking to do?</p>
  <div id="accordion-flush" @click="toggleAccordian" data-accordion="collapse" data-active-classes="bg-white dark:bg-gray-900 text-gray-900 dark:text-white" data-inactive-classes="text-gray-500 dark:text-gray-400">
    <div v-for="item in options">
      <RadioItem :item="item" />
    </div>
  </div>
</template>

<script setup>
  import RadioItem from './RadioItem.vue'
  const props = defineProps(['options'])
</script>

<style>
  @import 'tailwindcss/utilities.css';
</style>

