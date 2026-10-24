<script setup lang="ts">
const items = ref([
  {
    date: "October 24, 2026",
    title: "Security & Stability",
    description:
      "Strengthened API security, fixed attendance and export issues, and expanded end-to-end testing ahead of ClockUp 1.0.0.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/1.0.0-rc.x/security-and-stability",
  },
  {
    date: "October 18, 2026",
    title: "Release Candidate 1",
    description:
      "ClockUp reaches its first release candidate, with attendance status fixes and a refined production deployment workflow.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/1.0.0-rc.x/release-candidate",
  },
  {
    date: "October 16, 2026",
    title: "Introducing ClockUp",
    description:
      "A refreshed ClockUp identity, Filipino language support, faster admin navigation, and clearer camera consent notices.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/introducing-clockup",
  },
  {
    date: "October 13, 2026",
    title: "Holiday & Staff Management",
    description:
      "Introduced a holidays API and clock presets for staff creation, alongside improved OTP emails and client-side refinements.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/holiday-and-staff-management",
  },
  {
    date: "October 09, 2026",
    title: "Attendance & Realtime Improvements",
    description:
      "Improved attendance tracking with clock-out images, working-hours summaries, timezone settings, and real-time updates.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/attendance-and-realtime-improvements",
  },
  {
    date: "September 30, 2026",
    title: "Maintenance & Refinements",
    description:
      "Minor fixes, UI refinements, security improvements, and development workflow updates across ClockUp.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/maintenance-and-refinements",
  },
  {
    date: "September 24, 2026",
    title: "Attendance Data Export",
    description:
      "Download attendance records as PDF or Excel files for easier reporting and record keeping.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/attendance-data-export",
  },
  {
    date: "September 14, 2026",
    title: "Attendance Calendar",
    description:
      "Introducing a calendar-based system for easily filtering and navigating attendance records.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/attendance-calendar",
  },
  {
    date: "September 10, 2026",
    title: "Improve Infrastructure and Revamped Icon",
    description:
      " Improved ClockUp’s infrastructure with CI/CD, unit and E2E testing, and a more reliable development workflow, alongside minor fixes and refinements. ",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/improve-infrastructure",
  },
  {
    date: "September 01, 2026",
    title: "Legacy Integration Complete",
    description:
      "Completed the transition from ClockUp's legacy implementation to its new infrastructure and system architecture.",
    thumbnail: "/thumbnail/thumbnail.png",
    to: "/changelog/0.9.x/legacy-integration-complete",
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

    <UPageBody :ui="{ base: 'mx-auto max-w-6xl px-6 py-16' }">
      <UTimeline
        v-reveal
        :items="items"
        :default-value="999"
        size="xs"
        :ui="{
          title: 'sm:text-md md:text-lg lg:text-xl font-display ',
          description: 'sm:text-sm md:text-md lg:text-lg',
          date: 'sm:text-xs/5 md:text-sm/5 lg:text-md/5 text-black-500',
        }"
      >
        <template #description="{ item }">
          <span>
            {{ item.description }}
            <NuxtLink :to="item.to">
              <NuxtImg :src="item.thumbnail" class="mt-4 rounded-md" />
            </NuxtLink>
          </span>
        </template>
      </UTimeline>
    </UPageBody>
  </UPage>
</template>
