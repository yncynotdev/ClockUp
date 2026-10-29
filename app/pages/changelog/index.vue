<script setup lang="ts">
import type { BlogPostProps } from "@nuxt/ui";

const posts = ref<BlogPostProps[]>([
  {
    date: "October 28, 2026",
    title: "Clien-Side Security Patches",
    description:
      "Patched client-side credential handling, corrected vision-library integrity checks, and refined email verification and repository maintenance",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/1.0.0-rc.x/client-side-security-patches",
    badge: "v1.0.0-rc.3",
  },
  {
    date: "October 27, 2026",
    title: "Tooling Modernization",
    description:
      "Migrated to Vite+ and fixed the client CI workflow to keep release-candidate builds running smoothly.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/1.0.0-rc.x/tooling-modernization",
    badge: "v1.0.0-rc.2",
  },
  {
    date: "October 24, 2026",
    title: "Security & Stability",
    description:
      "Strengthened API security, fixed attendance and export issues, and expanded end-to-end testing ahead of ClockUp 1.0.0.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/1.0.0-rc.x/security-and-stability",
    badge: "v1.0.0-rc.1",
  },
  {
    date: "October 18, 2026",
    title: "Release Candidate 1",
    description:
      "ClockUp reaches its first release candidate, with attendance status fixes and a refined production deployment workflow.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/1.0.0-rc.x/release-candidate",
    badge: "v1.0.0-rc.0",
  },
  {
    date: "October 16, 2026",
    title: "Introducing ClockUp",
    description:
      "A refreshed ClockUp identity, Filipino language support, faster admin navigation, and clearer camera consent notices.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/introducing-clockup",
    badge: "v0.9.11",
  },
  {
    date: "October 13, 2026",
    title: "Holiday & Staff Management",
    description:
      "Introduced a holidays API and clock presets for staff creation, alongside improved OTP emails and client-side refinements.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/holiday-and-staff-management",
    badge: "v0.9.10",
  },
  {
    date: "October 09, 2026",
    title: "Attendance & Realtime Improvements",
    description:
      "Improved attendance tracking with clock-out images, working-hours summaries, timezone settings, and real-time updates.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/attendance-and-realtime-improvements",
    badge: "v0.9.9",
  },
  {
    date: "September 30, 2026",
    title: "Maintenance & Refinements",
    description:
      "Minor fixes, UI refinements, security improvements, and development workflow updates across ClockUp.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/maintenance-and-refinements",
    badge: "v0.9.8",
  },
  {
    date: "September 24, 2026",
    title: "Attendance Data Export",
    description:
      "Download attendance records as PDF or Excel files for easier reporting and record keeping.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/attendance-data-export",
    badge: "v0.9.7",
  },
  {
    date: "September 14, 2026",
    title: "Attendance Calendar",
    description:
      "Introducing a calendar-based system for easily filtering and navigating attendance records.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/attendance-calendar",
    badge: "v0.9.6",
  },
  {
    date: "September 10, 2026",
    title: "Improve Infrastructure and Revamped Icon",
    description:
      " Improved ClockUp’s infrastructure with CI/CD, unit and E2E testing, and a more reliable development workflow, alongside minor fixes and refinements. ",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/improve-infrastructure",
    badge: "v0.9.5",
  },
  {
    date: "September 01, 2026",
    title: "Legacy Integration Complete",
    description:
      "Completed the transition from ClockUp's legacy implementation to its new infrastructure and system architecture.",
    image: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/legacy-integration-complete",
    badge: "v0.9.4",
  },
]);
</script>

<template>
  <UPage>
    <UPageHero
      v-reveal
      title="Changelog"
      description="Follow the latest updates and improvements of ClockUp"
      :ui="{
        title: 'font-display font-normal',
      }"
    />

    <UPageBody :ui="{ base: 'mx-auto max-w-6xl px-6' }">
      <UBlogPosts orientation="vertical" :posts="posts" />
      <!-- <UTimeline -->
      <!--   v-reveal -->
      <!--   :items="items" -->
      <!--   :default-value="999" -->
      <!--   size="xs" -->
      <!--   :ui="{ -->
      <!--     title: 'sm:text-md md:text-lg lg:text-xl font-display ', -->
      <!--     description: 'sm:text-sm md:text-md lg:text-lg', -->
      <!--     date: 'sm:text-xs/5 md:text-sm/5 lg:text-md/5 text-black-500', -->
      <!--   }" -->
      <!-- > -->
      <!--   <template #description="{ item }"> -->
      <!--     <span> -->
      <!--       {{ item.description }} -->
      <!--       <NuxtLink :to="item.to"> -->
      <!--         <img :src="item.image" class="mt-4 rounded-md" /> -->
      <!--       </NuxtLink> -->
      <!--     </span> -->
      <!--   </template> -->
      <!-- </UTimeline> -->
    </UPageBody>
  </UPage>
</template>
