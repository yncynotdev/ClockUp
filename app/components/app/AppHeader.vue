<script setup lang="ts">
const appConfig = useAppConfig();

const runtimeConfig = useRuntimeConfig();

const navigation = [
  { label: "Home", to: "/" },
  // { label: "Contact", to: "#contact" },
  { label: "Changelog", to: "/changelog" },
];
</script>

<template>
  <UHeader :ui="{ root: ' backdrop-blur border-muted' }">
    <template #title>
      <div class="flex flew-row items-center gap-2.5">
        <NuxtImg src="/icon-180x180.png" class="size-9" />

        <NuxtLink to="/" class="font-display text-xl tracking-tight text-highlighted">
          ClockUp
        </NuxtLink>

        <UBadge variant="subtle">{{ appConfig.version }}</UBadge>
      </div>
    </template>

    <UNavigationMenu :items="navigation" class="hidden md:flex" />

    <template #right>
      <UColorModeButton class="hidden sm:inline-flex" />

      <UTooltip text="Open on GitHub" :kbds="['meta', 'G']" class="hidden sm:flex">
        <UButton
          color="neutral"
          variant="ghost"
          to="https://github.com/yncynotdev/ClockUp"
          target="_blank"
          icon="i-simple-icons-github"
          aria-label="GitHub"
        />
      </UTooltip>

      <UButton
        label="Open demo"
        :to="runtimeConfig.public.demo"
        target="_blank"
        trailing-icon="i-lucide-external-link"
        class="hidden md:inline-flex"
      />
    </template>

    <template #body>
      <UNavigationMenu :items="navigation" orientation="vertical" class="-mx-2.5" />
    </template>
  </UHeader>
</template>
