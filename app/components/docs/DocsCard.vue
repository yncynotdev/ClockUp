<script setup lang="ts">
const props = defineProps<{ content: string }>();
</script>

<template>
  <UPageCard :ui="{ root: 'p-4 sm:p-4 md:p-7' }">
    <Markdown>{{ content }}</Markdown>
  </UPageCard>
</template>
