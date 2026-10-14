<script setup>
import content from "./attendance-calendar.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
<DocsCard :content="content" />
</template>
