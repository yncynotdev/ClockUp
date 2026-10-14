<script setup>
import content from "./holiday-and-staff-management.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
<DocsCard :content="content" />
</template>
