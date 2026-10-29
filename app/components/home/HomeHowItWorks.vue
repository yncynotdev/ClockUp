<script setup lang="ts">
const runtimeConfig = useRuntimeConfig();

const clip = `${runtimeConfig.public.bucket}/landing_page/attendance-demo.mp4`;

const steps = [
  {
    title: "Take a picture",
    description: "The employee takes a face photo using the attendance camera.",
    icon: "i-lucide-camera",
  },
  {
    title: "Select your name",
    description: "Find your name quickly with search and filters.",
    icon: "i-lucide-keyboard",
  },
  {
    title: "Choose clock in or out",
    description: "They choose whether they are clocking in or clocking out.",
    icon: "i-lucide-log-in",
  },
  {
    title: "Submit attendance",
    description: "ClockUp records the attendance and marks whether the attempt was verified.",
    icon: "i-lucide-send",
  },
];
</script>

<template>
  <UPageSection
    id="how-it-works"
    v-reveal
    title="How it works"
    description="A simple four-step process for recording attendance."
    :ui="{
      root: 'py-16 sm:py-20',
      title: 'font-display font-normal tracking-[-0.02em]',
    }"
  >
    <div class="relative grid gap-4 sm:grid-cols-2 lg:grid-cols-4">
      <div
        class="absolute inset-x-[12.5%] top-[3.25rem] hidden h-px bg-gradient-to-r from-transparent via-primary/30 to-transparent lg:block"
        aria-hidden="true"
      />
      <UPageCard
        v-for="(step, index) in steps"
        :key="step.title"
        v-reveal="revealAt(index)"
        :ui="{ container: 'p-6' }"
      >
        <div class="relative flex flex-col gap-5">
          <div class="flex items-center justify-between">
            <div
              class="grid size-12 shrink-0 place-items-center rounded-2xl bg-primary/10 text-primary ring ring-primary/20"
            >
              <UIcon :name="step.icon" class="size-6" />
            </div>
            <span class="font-display text-4xl leading-none text-muted/60">
              {{ String(index + 1).padStart(2, "0") }}
            </span>
          </div>
          <div>
            <h3 class="font-display text-base font-normal text-highlighted">
              {{ step.title }}
            </h3>
            <p class="mt-2 text-sm leading-6 text-toned">
              {{ step.description }}
            </p>
          </div>
        </div>
      </UPageCard>
    </div>

    <video
      autoplay
      muted
      loop
      playsinline
      preload="metadata"
      class="bg-elevated rin ring-muted shadow-lg shadow-default/5 w-full"
    >
      <source :src="clip" type="video/mp4" />
    </video>
  </UPageSection>
</template>
