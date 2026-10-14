<script setup lang="ts">
import type { ButtonProps } from "@nuxt/ui";

const runtimeConfig = useRuntimeConfig();
const demoUrl = runtimeConfig.public.demoUrl;

const links = ref<ButtonProps[]>([
  {
    label: "Open demo",
    to: demoUrl,
    target: "_blank",
    trailingIcon: "i-lucide-external-link",
  },
  {
    label: "How it works",
    to: "#how-it-works",
    color: "neutral",
    variant: "subtle",
    trailingIcon: "i-lucide-arrow-down",
  },
]);

const ui = {
  //  root: "overflow-hidden",
  container: "min-h-[calc(100vh-var(--ui-header-height))] ",
  //  wrapper: "max-w-3xl",
  headline: "font-display text-lg font-normal",
  title: "font-display font-normal tracking-[-0.03em] text-balance sm:text-6xl lg:text-7xl",
  links: "gap-3",
};
</script>

<template>
  <UPageHero
    v-reveal
    as="section"
    headline="ClockUp"
    title="Modern and friendly camera-based attendance."
    description="Simplify attendance with fast, reliable clock-ins and clock-outs using face-based verification. Built for businesses that wants to migrate from paper-based to reliable and efficient way of recording attendances."
    :links="links"
    :ui="ui"
  >
    <template #top>
      <HomeHeroCubes />
    </template>
  </UPageHero>
</template>
