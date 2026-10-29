<script setup lang="ts">
const runtimeConfig = useRuntimeConfig();
</script>

<template>
  <UPageCTA
    v-reveal
    title="See ClockUp in action"
    description="Explore the demo and see how ClockUp handles the attendance workflow."
    :links="[
      {
        label: 'Open demo',
        to: runtimeConfig.public.demo,
        target: '_blank',
        trailingIcon: 'i-lucide-external-link',
      },
    ]"
    :ui="{
      title: 'font-display font-normal tracking-[-0.02em]',
    }"
  />
</template>
